# Product Planning

Planning takes place in several different ways. How planning is done depends on the maturity of the project and team, the client's project structure, the existing backlog and release plans, and the specifics of the project. 

# Release Planning
In general, the client should know a general release plan for some amount of future timeline. For some projects, this could be 3 months. Others might have a release timeline that is determined week by week. These differences should be driven by the needs of the client and state of the project.

# Daily Schedule

## Daily Standup
We do daily standups to ensure that teams are communicating about work in progress, eliminating blockers, and warning of potential risk. Oftentimes, standups become simple recitations about what we did yesterday and what we are going to do today. Although this information can be useful, it's important not to just to go through the motions. Instead, highlight areas of concern, reveal bottlenecks, and focus on the flow of work in progress. "Walking the board" is a helpful way to do this. Starting with the right hand column of the Kanban board, briefly look at each card and ensure that it's progress is unencumbered. Standups should be time to reveal problems with the flow. Commonly, columns that are blocked, or violating WIP, are revealed during this time. For example, a backlogged "Acceptance" column can lead the team to make decisions like stopping work until it has been cleared out.

## Testing and Accepting
In general, code is pushed to a staging environment whenever the feature is deemed finished by the development team. Although we often attempt to use the Kanban "pull" system, it usually makes sense to put the card into Testing/Acceptance when the code is pushed. Another option is to mark a card as "ready to be pulled" so that a push is not needed. Hopefully the client is integrated into the project such that they're aware of the updated card state. If not, standup is a good time to communicate these things. The client should be accepting these stories within a day of them being moved to staging. If this is delayed, unverified work accumulates, resulting in a lot of risk. Circumstances occasionally do cause a delay in acceptance, but attempts should be made to minimize this. A WIP limit should be placed on Testing/Acceptance, and violation of the limit should be consideration for stopping work, in some circumstances.

## Rejecting
Stories may be rejected for several reasons. Usually the client informs the team of issues encountered during standup. Rejection reasons should be documented on the card, along with needed reproduction steps. Unless the fix is extremely simple, the card should be moved back into "Development". This shows that the feature still falls under WIP and should be fixed immediately. Occasionally the rejected story could be moved to "Up Next", but this essentially increases WIP. One potentially dangerous pattern is for the rejected story to actually be accepted and moved to "Done", and then for a defect to be filed for the rejection reason. Features should only be accepted when they're functional and designed well.


