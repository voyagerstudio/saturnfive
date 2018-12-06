# Saturn V Documentation 
> A design system springboard with three distinct levels of fidelity and opinionated code.

## Quick Facts:
* **Saturn V is not a bootstrap competitor.** Saturn V is built with the intention of writing easier/faster CSS, not avoiding the task altogether (not that I'm knocking bootstrap _at all_). The most complex component you'll see in Saturn V for example is styling buttons.
* **Saturn V is not a matured design system.** Saturn V is designed to help you get going with your own design system, it's a springboard but not the real thing. Modifying the settings via the SCSS Variables/Tokens will help get you through the initial set up but there will still be plenty to do in your own projects (the good thing is Saturn V shouldn't establish any meaningful amount of technical debt)
* You can use Saturn V in both big and small projects. It's my go-to foundation for new projects of all sizes, I just don't always override any of the settings for the smaller projects. 
* Almost everything in Saturn V from the type scale ratio to the number of generated lighter and darker color options is configurable. All you have to do is before importing Saturn V define your own values for the corresponding SCSS variables. 

For a quick cheat sheet guide on using Saturn V, use this [temporary reference sheet](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md). 


## How to get started
Getting started with Saturn V is easy, just treat it as any other SCSS partial. Saturn V should be imported before anything that would utlize it's feature or be impacted by it's default styles. Any Saturn V overrides should also be imported or written before importing Saturn V in order to take effect.

Once Saturn V is added to your codebase (either manually or via npm), just import which stage of Saturn V you'd like to use. 

### Stage 01
Saturn Five Stage One has almost no opinion on what your design aesthetic will look like. in this stage, the tokens and tools get imported but nothing else. This means importing just stage 01 will not increase your compiled css at all until you start using it's styles in your own code. 

### Stage 02
Saturn Five Stage Two builds on what's available in stage one by adding new utilities and configurable patterns. In this stage, you'll start to see things like media query or accessibility support as well as mixins for setting type and shadows.

### Stage 03
Saturn Five Stage Three ties together stage one and stage two by adding the necessary resets and more complex patterns. In this final stage, you'll finally see styles that will compile into CSS and design decisions wrapped in more complex mixins such as buttons, links, form fields, and more.


## Using Saturn V in your project
To start using Saturn V, just import _*one of*_ the stages you would like to use, eg:

```SCSS
// "my-custom-saturnfive-overrides"
@import 'satfive-overrides';

// Stage One
@import '@/saturnfive/stage-01';

// OR

// Stage Two
@import '@/saturnfive/stage-02';

// OR

// Stage Three
@import '@/saturnfive/stage-03';
```
