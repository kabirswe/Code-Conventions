# HTML Code Conventions [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE)


## Close All HTML Elements
```html
==> Bad
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
<meta charset="utf-8">
==> Good 
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
<meta charset="utf-8"/>
```
## Spaces and Equal Signs 
```html
==> Bad
<link rel = "stylesheet" href = "styles.css">
==> Good
<link rel="stylesheet" href="styles.css">
```
## Blank Lines and Indentation
Do not add blank lines without a reason.
```html
==> Bad
<div>

  <h1>Famous Cities</h1>

  <h2>Tokyo</h2>

  <p>
	Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
	and the most populous metropolitan area in the world.
	It is the seat of the Japanese government and the Imperial Palace,
	and the home of the Japanese Imperial Family.
  </p>

</div>

// Good
<body>

<h1>Famous Cities</h1>

<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.
It is the seat of the Japanese government and the Imperial Palace,
and the home of the Japanese Imperial Family.</p>

</body>
```
## Do not use entity references.
```html
<!-- Bad -->
The currency symbol for the Euro is &ldquo;&eur;&rdquo;.
<!-- Good-->
The currency symbol for the Euro is "€".

```
## Break long lines (optional). // we can remove this one
```html
// Bad
<md-progress-circular md-mode="indeterminate" class="md-accent"
    ng-show="ctrl.loading" md-diameter="35">
</md-progress-circular>
// Good
<md-progress-circular
    md-mode="indeterminate"
    class="md-accent"
    ng-show="ctrl.loading"
    md-diameter="35">
</md-progress-circular>
```
### License

React is [MIT licensed](./LICENSE).