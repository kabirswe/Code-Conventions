# CSS Code Conventions [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE)


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
## Don’t use camelCase for class name
```css
==> Bad
.activeArticleDetails{
 //......
}
==> Good
.active-article-details{
// .......
}
```
## Try to avoid more than two words for a given name
```css
.button {
  /* OK */
}
.dropdown-button {
  /* still OK */
}
.dropdown-button-part-one {
  /* Hmm, still ok, but will be unredable when adding children */
}
.dropdown-button-part-one__button-admin {
  /* Not Ok */
}
```
## Use has- or is- prefix for the state
```css
.activated {
  /* Bad */
}
.is-activated {
  /* Good */
}
```
## Use ID and class names that are as short as possible but as long as necessary.
```css
==> Bad
#navigation {}
.atr {}

==>Good */
#nav {}
.author {}
```
## Avoid qualifying ID and class names with type selectors.
```css
==> Bad
ul#example {}
div.error {}

==> Good
#example {}
.error {}
```
## Use shorthand properties where possible.
```css
==> Bad
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;

==> Good
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```
## Declaration Block Separation
```css
/* Bad: missing space */
#video{
  margin-top: 1em;
}

/* Bad: unnecessary line break */
#video
{
  margin-top: 1em;
}

/* Good */
#video {
  margin-top: 1em;
}
```
## CSS Quotation Marks
```css
==> Bad
@import url("https://www.google.com/css/maia.css");

html {
  font-family: "open sans", arial, sans-serif;
}
==> Good
@import url(https://www.google.com/css/maia.css);

html {
  font-family: 'open sans', arial, sans-serif;
}
```
### License

React is [MIT licensed](./LICENSE).