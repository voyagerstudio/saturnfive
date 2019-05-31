# Saturn V Documentation 
A design system springboard.

## Quick Facts:
* **Saturn V is not a bootstrap competitor.** Saturn V is built with the intention of writing easier/faster CSS, not avoiding the task altogether (not that I'm knocking bootstrap _at all_). The most complex component you'll see in Saturn V for example is styling buttons.
* **Saturn V is not a matured design system.** Saturn V is designed to help you get going with your own design system, it's a springboard but not the real thing. Modifying the settings via the SCSS Variables/Tokens will help get you through the initial set up but there will still be plenty to do in your own projects (the good thing is Saturn V shouldn't establish any meaningful amount of technical debt)
* You can use Saturn V in both big and small projects. It's my go-to foundation for new projects of all sizes, I just don't always override any of the settings for the smaller projects. 
* Almost everything in Saturn V from the type scale ratio to the number of generated lighter and darker color options is configurable. All you have to do is before importing Saturn V define your own values for the corresponding SCSS variables. 


## How to get started
Getting started with Saturn V is easy, just treat it as any other SCSS partial. Saturn V should be imported before anything that would utlize it's feature or be impacted by it's default styles. Any Saturn V overrides should also be imported or written before importing Saturn V in order to take effect.
