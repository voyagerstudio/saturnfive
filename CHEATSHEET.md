# Saturn V Cheat sheet
This is a quick guide that documents the various functions and mixins along with their arguments. With the exception of your own overrides for Saturn V tokens, Saturn V should be imported before your own SCSS. Saturn V operates under the assumption that the root font size on `html` is `100%` or `16px`. If you want to experiment with Saturn V, you can use this [template codepen as a playground (based on version 0.4.0)](https://codepen.io/pen?template=zJVQNK). 

## Table of Contents:
* [Stage 001](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#saturn-v--stage-001)
  * [Tokens](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#tokens)
    * [Color](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#color-tokens)
    * [Type](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#type-tokens)
    * [Base units](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#base-unit-tokens)
    * [Z-Index](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#z-index-default)
  * [Features](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#features)
    * [Color](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#color)
    * [Units](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#units)
    * [Shadow](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#shadows)
    * [Gradient](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#simple-gradient)
    * [Type Scale](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#font-scale)
    * [Z-Index](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#z-index)
* [Stage 002](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#saturn-v--stage-002)
  * [Utilities](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#utilities)
    * [Focusable-Only](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#focusable-only)
    * [Disable Text Selection](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#disable-text-select)
    * [Share Pixel Value](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#share-px-val)
  * [Patterns](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#patterns)
    * [Set Type](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#set-type)
    * [Z-Index](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#z-index-1)
    * [Shadows](https://github.com/voyagerstudio/saturnfive/blob/golden-source/CHEATSHEET.md#shadows-1)
* Stage 003 

---
## Saturn V — Stage 001

### Tokens
To override tokens, make sure you set a new value _before_ your import of Saturn V.

#### Color Tokens
* `$s5_color-brand-color-1` - default primary brand color
* `$s5_color-brand-color-2` - default secondary brand color
* `$s5_color-brand-color-3` - default tertiary brand color
* `$s5_color-soft-white` - off white
* `$s5_color-soft-black` - a dark shade that isn't quite a harsh black
* `$s5_color-focus-base` - a default color for focus
* `$s5_color-info-base` - a default color for highlighting info
* `$s5_color-alert-base` - a default color for highlighting alerts
* `$s5_color-warning-base` - a default color for highlighting warnings
* `$s5_color-danger-base` - a default color for highlighting strong warnings
* `$s5_color-success-base` - a default color for highlighting success messages
* `$s5_color-scale-step-total` - this modifies how many colors are generated with the color feature. By default, this variable is set to 19 meaning the base color, 9 darker colors, and 9 lighter colors. This can be set to any number larger than 5 as long as it is a negative number.  

#### Type Tokens
* `s5_fontstack--monospace` - monospace fontstack
* `s5_fontstack--sans-serif` - sans-serif default
* `s5_fontstack--serif` - serif default
* `s5_fontstack--display` - fontstack for displays, eg headings
* `s5_fontstack--masthead` - fontstack for masthead text
* `s5_fontstack--body` - fontstack default for body text
* `s5_fontstack--code` - fontstack default for code text
* `s5_fontstack--interface` - fontstack default for interface elements (eg buttons, forms)
* `s5_fontstack--caption` - fontstack default for caption text
* `s5_fontstack--aside` - fontstack default for aside text
* `s5_fontstack--blockquote` - fontstack default for blockquote text


* `s5_weight--thin` - thin font weight
* `s5_weight--extra-light` - extra-light font weight
* `s5_weight--light` - light font weight
* `s5_weight--book` - book font weight
* `s5_weight--medium` - medium font weight
* `s5_weight--demi-bold` - demi-bold font weight
* `s5_weight--bold` - bold font weight
* `s5_weight--heavy` - heavy font weight
* `s5_weight--black` - black font weight


* `s5_line-height-xs` - x-small line-height
* `s5_line-height-sm` - small line-height
* `s5_line-height-md` - medium line-height
* `s5_line-height-lg` - large line-height
* `s5_line-height-xl` - x-large line-height

* `s5_font-scale-modifier` - ratio that each font-scale step is increased by. (default is 1.125)
* `s5_font-scale-base` - set the default base font size for the font scale. This is the lowest font size the scale will use (font-size(1);)
* `s5_font-root-size: this is used to calculate rem based on the font-size of `html`. If you change the html font size, also change this variable.

#### Base Unit Tokens
* `s5_foundation-unit-size` - a multiplier used by the size-multiplier mixin. This lets you create uniform units in multiples of four

#### Media Queries
* `$s5_viewport-micro` - smallest viewport size
* `$s5_viewport-xs` - x-small viewport size
* `$s5_viewport-sm` - small viewport size
* `$s5_viewport-md` - medium viewport size
* `$s5_viewport-lg` - large viewport size
* `$s5_viewport-xl` - x-large viewport size
* `$s5_viewport-massive` - massive viewport size

#### Z-index default
* `$z-order` - this is a list of strings that should match up with different parts of your UI. The order from first to last will assign z-index values going from highest to lowest. (essentially, top on the list is also top on the stack)

---
### Features

#### Color
```scss
//set-color($name, $shade:0, $alpha:1)
// $shade options: -9 to 9
// $name options: anything in color map, by default any of the 147 css color names

.example-div {
  color:set-color(red);
  background-color:set-color(blue, 9);
  border: 1px solidset-color(green, -2, 0.5);
}
```

#### Units
```scss

// strip-unit($number)
// (removes unit, eg turns '20px' into '20')

// px($size)
// converts a px size to rem based on $s5_font-root-size: 16px, eg px(10) = 0.625rem

// pow($number, $power)
// calculates power. $number^$power, eg pow(3,3) = 27

```

#### Size Multiplier
```scss

// set-size($multiplier)
// sets value as multiplier of base size (default is 4px). Also includes arguments for 'pixel' (1px) and 'micro' (2px). 

// eg input
margin-bottom: set-size(10);

// output
margin-bottom: 40px; // technically sets in rem


```

#### Debug 
```scss

// @include debug-overlay($type, $location, $opacity, $offset-x, $offset-y);
// $type options: grid, more to come
// $location options: local (when used as property), global (sets on html for the whole page)
// $opacity: 0%-100%
// offset-x: offset pixel amount on horizontal plane
// offset-y: offset pixel amount on vertical plane

```

#### Shadows
```scss

// shadow($step:0, $color:black, $intensity-multiplier:1)
// step options: 0-20

.example-div {
  box-shadow: shadow(5, red, 1.5);
}

```

#### Simple Gradient
```scss

// simple-gradient($gradient-color, $lightness:base)
// lightness options: darkest, darker, dark, base, light, lighter, lightest

.example-div {
  background: simple-gradient(red, dark);
}
```

#### Font Scale
```scss

// font-scale($step)
// $step options: 1-infinite

.example-div {
  font-size: font-scale(5);
}
```

#### Z Index
```scss

// z-index-output($object)
// $object options: anything from the list stored in $z-order variable

.example-div {
  z-index: z-index-output(example-one);
}
```

---
## Saturn V — Stage 002

### Utilities

#### Media Queries
`@include min-view($size) { properties }` or `@include max-view($size) { properties }`. `$size` options include: micro, xs, sm, md, lg, xl, massive. 

#### Focusable Only
`@include focusable-only;` - Styles dom element so that it is hidden and only accessible to screen readers and to sighted users via focusing with keyboard navigation.

#### Disable Text Select
`@include disable-text-select;` - disables the users ability to select text with this mixin applied. 

#### Share px Val
```scss

// @include share-px-val($props...)
// eg: @include share-px-val(margin-top, margin-left, margin-right, 10) - will add margin-top, margin-left, and margin-right properties with 10px converted to rem

```

#### Screen Reader Only
`@include screen-reader-only;` will make dom element content only accessible via a screen reader. 

---
### Patterns

#### Set-Type
```scss

// @include set-type($context:body, $font-scale:5, $weight:book, $style:normal)
// $context options: body, masthead, display, code, interface, caption, aside, blockquote
// $font-scale options: 1-infinite (5 is ~16px by default)
// $weight options: thin, extra-light, light, book, medium, demi-bold, bold, heavy, black
// $style options: normal, italic, oblique

.example-div {
  @include set-type(display, 10, heavy, italic);
}

```

#### Z-Index
```scss

// @include z-index($object)

.example-div {
  @include-z-index(example-one);
}

```

#### Shadows
```scss

// @include standard-shadow($step:0, $color:black, $intensity-multiplier:1)
// essentially the same as the function, but wrapped in a mixin

// @include interactive-shadow($step:0, $color:black, $intensity-multiplier:1, $border-radius:0, $aniamtion-speed: 75ms, $animation-type:ease-in)

```

---
## Saturn V — Stage 003

### Base
These are some base styles to establish global properties such as box-sizing.

### A11y
these styles establish the baseline for accessibility such as `ARIA-hidden` or `disabled` styling.
