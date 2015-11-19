# Responsive Grid

A responsive, mobile first grid system with up to five breakpoints and fixed gutters.

### Requirements

Built with Sass. No other dependancies or libraries required.

```
Sass >= 3.4
```

### Config

This is everything you need.

If you want to only have less than five breakpoints, set two or more width variables to the same value.

If you want to rename your classes so they are name-spaced, you can do that too.

```
//* GRID CONFIG *
$universal_gutter_width: 20px;
$total_columns: 12;

//* BODY PADDING *
$body_padding: $universal_gutter_width;

//* BREAKPOINTS (px) *
$max_width: 1280px;
$lg_width: 1024px;
$md_width: 768px;
$sm_width: 400px;

//* BREAKPOINTS (%) *
$min_width: 90%;
$min_gutter: 2%;

//* CLASS NAMES *
$class-container: "container";
$class-row: "row";
$class-column: "col";
$class-push: "push";
$class-overflow: "cols";
$class-width-pixel: "w";
$class-width-percent: "inner";
```

### Breakpoint Helpers

This also creates some breakpoint mixins based on your breakpoint widths that you can use if you like.

```
@include bp-sm {
  // Applied to > $sm_width
}
@include bp-md {
  // Applied to > $md_width
}
@include bp-lg {
  // Applied to > $lg_width
}
@include bp-max {
  // Applied to > $max_width
}
```

Or if you want to make you own there is also a media mixin.

```
$media_query: "screen and (max-width: 960px)";

@include media($media_query) {
  // Some CSS
}

```

### Credits/Inspiration:

This started with and was inspired by Profound Grid. But ended up somewhere else.

Profound Grid: http://www.profoundgrid.com
