# HTML Code Conventions [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE)


## Formatting

* Use soft tabs (2 spaces) for indentation.
* Names are written in lowercase Latin letters.
* Words are separated by a hyphen (-).
* Prefer dashes over camelCasing in class names.
* When using multiple selectors one rule declaration, give each selector its own line.
* Put a space before the opening brace { in rule declarations.
* In properties, put a space after, but not before, the : character.
* Put closing braces } of rule declarations on a new line.
* Put blank lines between rule declarations.

## Try to use one selector per line

```css
==> Bad
.avatar{
    border-radius:50%;
    border:2px solid white;
 }
.no, .nope, .not_good {
   // ...
}
#lol-no {
  // ...
}

==> Good
.avatar {
  border-radius: 50%;
  border: 2px solid white;
}
.one,
.selector,
.per-line {
  // ...
}
```
## For Border I think border none is good

```css
==> Bad
.foo {
  border: none;
}

==> Good
.foo {
  border: 0;
}
```
## Ordering of property declarations
1. Property declarations
List all standard property declarations, anything that isn't an @include or a nested selector.


```css
.btn-green {
  background: green;
  font-weight: bold;
  // ...
}
```
2. Placed @include at the end makes it easier to read the entire selector.

```css
.btn-green {
  background: green;
  font-weight: bold;
  @include transition(background 0.5s ease);
  // ...
}
```
3. For Nested Selectors

```css
.btn {
  background: green;
  font-weight: bold;
  @include transition(background 0.5s ease);

  .icon {
    margin-right: 10px;
  }
}
```

## Naming Conventions
1. Regarding variables, functions and mixins used lowercase hyphen-delimited, and camelCase(for css module only)  and above all meaningful.

```css
$vertical-rhythm-baseline: 1.5rem; 
@mixin size($width, $height: $width) {
  // ...
}
@function opposite-direction($direction) {
    // ...
}
```
2. For constants used all-caps snakerized variables
```css
==> Bad
$css-positions: (top, right, bottom, left, center);
==> Good
$CSS_POSITIONS: (top, right, bottom, left, center);
```

### License

React is [MIT licensed](./LICENSE).