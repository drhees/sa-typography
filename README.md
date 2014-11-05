# SA Typography

Inspried by the Guardian [Guss](https://github.com/guardian/guss) collection.

## Installation

```
bower install <repo_name> --save
```

```scss
// Override defaults if needed
$f-header-text: 'Lato', 'Helvetica Neue', Helvetica, Arial, 'Lucida Grande', sans-serif !default;
$f-body-text: 'Lato', 'Helvetica Neue', Helvetica, Arial, 'Lucida Grande', sans-serif !default;

$font-scale: (
    header: (
        1: (font-size: 14, line-height: 18),
        2: (font-size: 16, line-height: 20),
        3: (font-size: 20, line-height: 24),
        4: (font-size: 24, line-height: 28),
        5: (font-size: 28, line-height: 32),
        6: (font-size: 32, line-height: 36),
        7: (font-size: 36, line-height: 40),
        8: (font-size: 40, line-height: 44),
        9: (font-size: 44, line-height: 48),
    ),
    body: (
        1: (font-size: 12, line-height: 18),
        2: (font-size: 14, line-height: 20),
        3: (font-size: 16, line-height: 22), //.lrg
        4: (font-size: 18, line-height: 26), //.xlrg
    ),
);


@import 'path/to/_typography.scss';
```

## Suggested default type settings

To kick start a project with scalable typography,
here are the suggested default global type settings:

```scss
@include sa-typography-defaults;
```

Compiles to:

```css
html {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    font-size: 62.5%;
    font-size: calc(1em * .625);
}
body {
    font-size: 1.6em;
    line-height: 1.5;
}
```

## Usage

Refer yourself to the matrix below, using these principles:

```scss
h1 {
    @include fs-headline(4);
}
p {
    @include fs-bodyCopy(3);
}
.small-text {
    // Output font-size and line-height only
    @include fs-bodyCopy(1, $size-only: true);
}
.body-heading {
    // Output font family and weight settings only
    @include f-bodyHeading;
}
.get-font-size {
    font-size: get-font-size(headline, 6);
}
.get-line-height {
    line-height: get-line-height(header, 3);
}
```

## Features

Provides Sass mixins and values for SA typography & font scale.

![Font scale](font-scale.png)