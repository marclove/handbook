# Tools and Techniques

## Overview

This section of the handbook discusses our tools, techniques, and practices for
doing work.  This is not exclusive to specific roles within the company, but
some topics may be more relevant to your work than others.

## CSS Style Frameworks

### Foundation

Gaslight prefers to use the [Zurb Foundation framework](http://foundation.zurb.com/) for:

  * Laying out page elements in a responsive grid
  * Bootstrapping a baseline of element styles
  * Providing useful website components (e.g. tooltips, modals, navigation
    widgets)

### Rational

Advantages:

  * Foundation uses Sass, which is the preferred precompiler language for CSS.
  * Foundation's grid framework provides responsive functionality with little
    additional work.
  * Foundation's grid works with Ember.js which litters your DOM with script
    tags.

Disadvantages:

  * Elements receive default styling even without any classes applied. This
    makes it difficult to introduce custom styles without overriding many
    styles.
  * Styles tend to be defined using positional selectors, making it very
    difficult to build on existing Foundation styles.
  * Foundation doesn't use any namspacing patterns as found in
    [SMACCS](http://smacss.com/), or [other evolving
    patterns](https://gist.github.com/necolas/1309546) to manage css classes.
    This makes adding to their styles difficult.

Why not Bootstrap?

  * Bootstrap is written in Less.js, which doesn't mesh well with our Sass
    preference.
  * Bootstrap's grid framework doesn't work well with Ember Metamorphs.

Why not Bourbon & Bourbon Neat?

  * Bourbon does not provide default styles and JavaScript components which are
    useful for rapid UI development without custom style.


## Full-Stack Integration Testing

### Cucumber & Capybara

For full-stack integration testing of Ruby on Rails applications, Gaslight
prefers using Cucumber and Capybara.

