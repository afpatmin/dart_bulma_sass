# [bulma_sass](https://bulma.io)

[Bulma](https://bulma.io/) is a **modern SCSS framework** based on [Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes).

## Usage

Add Sass and Builder runner to the project pubspec.yaml:
```yaml
dev_dependencies:
  build_runner: ^0.7.10+1
  sass_builder: ^1.1.2
```

```scss
// 1. Import the initial variables
@import "packages/bulma_sass/scss/utilities/initial-variables";
@import "packages/bulma_sass/scss/utilities/functions";

// 2. Set your own initial variables
// Update blue
$blue: #72d0eb;
// Add pink and its invert
$pink: #ffb3b3;
$pink-invert: #fff;
// Add a serif family
$family-serif: "Merriweather", "Georgia", serif;

// 3. Set the derived variables
// Use the new pink as the primary color
$primary: $pink;
$primary-invert: $pink-invert;
// Use the existing orange as the danger color
$danger: $orange;
// Use the new serif family
$family-primary: $family-serif;

// 4. Setup your Custom Colors
$linkedin: #0077b5;
$linkedin-invert: findColorInvert($linkedin);
$twitter: #55acee;
$twitter-invert: findColorInvert($twitter);
$github: #333;
$github-invert: findColorInvert($github);

// 5. Add new color variables to the color map.
@import "packages/bulma_sass/scss/utilities/derived-variables";
$addColors: (
  "twitter":($twitter, $twitter-invert),
  "linkedin": ($linkedin, $linkedin-invert),
  "github": ($github, $github-invert)
);
$colors: map-merge($colors, $addColors);

// 6. Import the rest of Bulma
@import "packages/bulma_sass/scss/bulma";
```

## Documentation

Documentation for the Bulma framework can be found here [Bulma Documentation](https://bulma.io/documentation)

## Bugs and Features

Report problems with this package to [https://github.com/indiealexh/dart_bulma_sass](https://github.com/indiealexh/dart_bulma_sass)

Report problems with the core framework to [https://github.com/jgthms/bulma](https://github.com/jgthms/bulma)

## Copyright and license
Dart package is released under MIT license.

Original Code copyright 2017 Jeremy Thomas and released under [the MIT license](https://github.com/jgthms/bulma/blob/master/LICENSE).