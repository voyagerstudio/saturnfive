# Saturn V
A design system springboard with three distinct levels of fidelity and opinionated code. This project has recently been completely overhauled and is back in a less stable state. SV is _usable_ but:

⚠️ _**future releases may include breaking changes**_ ⚠️


# Getting started

## Understanding the three stages of Saturn V
to get started with Saturn V, first choose which level of fidelity you will want to start your project with. Stage-01 includes a series of useful snippets and shortcuts to get to design decisions fast without siloing your choices too strictly. Stage-01 has almost no opinion on what your design aesthetic will look like.

Stage-02 Builds on the tools available on Stage-01 and starts to establish more opinionated design patterns such as buttons and forms. Although Stage-02 starts to establish the start of a design language, the only code that compiles is what you explicitly reference in your own codebase. 

Stage-03 is still being developed conceptually but will be the final stage that establishes a class strucuture and more custom styled patterns and components. 

## Using Saturn V in your project
To start using Saturn V, just import the specific stage you would like to use, eg:

```SCSS
// Stage One
@import 'saturnfive/SV-SI';

// Stage Two
@import 'saturnfive/SV-SII';

// Stage Three
@import 'saturnfive/SV-SIII';
```
