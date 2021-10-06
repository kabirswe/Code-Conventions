# [HTML Code Conventions][![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE)


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
//Bad
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
//Good
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

This example will render "Hello Taylor" into a container on the page.

You'll notice that we used an HTML-like syntax; [we call it JSX](https://reactjs.org/docs/introducing-jsx.html). JSX is not required to use React, but it makes code more readable, and writing it feels like writing HTML. If you're using React as a `<script>` tag, read [this section](https://reactjs.org/docs/add-react-to-a-website.html#optional-try-react-with-jsx) on integrating JSX; otherwise, the [recommended JavaScript toolchains](https://reactjs.org/docs/create-a-new-react-app.html) handle it automatically.

## Contributing

The main purpose of this repository is to continue evolving React core, making it faster and easier to use. Development of React happens in the open on GitHub, and we are grateful to the community for contributing bugfixes and improvements. Read below to learn how you can take part in improving React.

### [Code of Conduct](https://code.fb.com/codeofconduct)



### License

React is [MIT licensed](./LICENSE).