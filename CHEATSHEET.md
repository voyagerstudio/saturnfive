# Saturn V Cheat sheet
This is a quick guide that documents the various functions and mixins along with their arguments.

---
## Saturn V — Stage 001

### Features

**Color**
```scss
// color($name, $shade:0, $alpha:1)
// $shade options: -9 to 9
// $name options: anything in color map, by default any of the 147 css color names

.example-div {
  color: color(red);
  background-color: color(blue, 9);
  border: 1px solid color(green, -2, 0.5);
}
```

**Units**
```scss

// strip-unit($number)
// (removes unit, eg turns '20px' into '20')

// px($size)
// converts a px size to rem based on $s5_font-root-size: 16px, eg px(10) = 0.625rem

// pow($number, $power)
// calculates power. $number^$power, eg pow(3,3) = 27

```

**Shadows**
```scss

// shadow($step:0, $color:black, $intensity-multiplier:1)
// step options: 0-20

.example-div {
  box-shadow: shadow(5, red, 1.5);
}

```

**Simple Gradient**
```scss

// simple-gradient($gradient-color, $lightness:base)
// lightness options: darkest, darker, dark, base, light, lighter, lightest

.example-div {
  background: simple-gradient(red, dark);
}
```

**Font Scale**
```scss

// font-scale($step)
// $step options: 1-infinite

.example-div {
  font-size: font-scale(5);
}
```

