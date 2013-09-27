# Hotfixes

## Using a feature branch for the hotfix

If you know you need to create a fix for production that will also need to be applied to master, here's the procedure:

1. Find the best common ancestor between production and master:

    `git merge-base v3 master`

2. Create a new "hotfix" branch from that ancestor commit (but use a better name for the bug as the branch name).

    `git checkout -b hotfix <whatever you got from merge-base>`

3. Commit your code changes to that "hotfix" branch

4. Merge that hotfix branch into production

    `git checkout v3 && git merge --no-ff hotfix`

5. Merge that hotfix branch into master

    `git checkout master && git merge --no-ff hotfix`

```
        v3--------v3 (hotfixed)
       /         /
ancestor----hotfix
       \         \
        master----master (hotfixed)
```

The --no-ff flag keeps the hotfix branch label at the hotfix tip, instead of pulling the label to v3 or master.

The source for this procedure is a [comment on stackoverflow](http://stackoverflow.com/questions/10761348/git-merging-hotfix-to-multiple-branches/10761836#10761836)

## Making the fix directly on the production branch

This is generally a bad idea. In order to get the code back into master, it has to be cherry picked. When cherry picking
code, it generates a new sha. That means there are actually two commits in the repo for the same change: one on production
and one on master.

To determine which commits are on production and not on master you can use `git cherry`:

```
$ git cherry -v master production
- 30c657915c87f2b70fb594e9fc75e4758b052dcf report schedule UI tweak
+ a03d857120e8e2ccaa9b389bb2bb18db25b0f7d7 Change timer page title for dispense and restock
+ 84cbd529d624f574d161550a4b06e5cb8d57e9ef Fix issue with passenger forks improperly connecting to redis
```

This is showing three commits made directly on `production`. One of them (30c65791) was made on production and cherry picked
onto master. The leading `-` indicates an "equivalent commit" between the two branches. The other two commits have yet to 
be picked into master.

```
$ git checkout master
$ git cherry-pick a03d857120e8e2ccaa9b389bb2bb18db25b0f7d7
$ git cherry-pick 84cbd529d624f574d161550a4b06e5cb8d57e9ef
$ git cherry -v master production
- 30c657915c87f2b70fb594e9fc75e4758b052dcf report schedule UI tweak
- a03d857120e8e2ccaa9b389bb2bb18db25b0f7d7 Change timer page title for dispense and restock
- 84cbd529d624f574d161550a4b06e5cb8d57e9ef Fix issue with passenger forks improperly connecting to redis
```

Now all three commits made directly to production have equivalent commits on master.
