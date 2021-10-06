# React Js Code Conventions [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE)


## Component Structure:
If you have internal state or refs follow:-
```jsx
class Listing extends React.Component {
  // ...
  render() {
    return <div>{this.state.hello}</div>;
  }
}
```
If you don’t have internal state or refs follow:-
```jsx
function Listing({ hello }) {
  return <div>{hello}</div>;
}
```
## Naming
```jsx
a. Extensions: Use .jsx
b. FileName: Use PascalCase (E.g. FileName.jsx)
c. Reference Naming: Use PascalCase for React Component File Naming and camelCase for their reference.
    1. import ReservationCard from './ReservationCard';
    2. const reservationItem = <ReservationCard />;
```
## Component Naming
Use the filename as the component name. For example, name:
```jsx
==> bad
import Footer from './Footer/Footer';

==> good
import Footer from './Footer';

```
## Declaration
```jsx
export default class ReservationCard extends React.Component {
}
```
## Alignment
```jsx
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
/>
// if props fit in one line then keep it on the same line
<Foo bar="bar" />
// children get indented normally
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
>
......
</Foo>
```
## Spacing
Always include a single space in your self-closing tag. eslint: 
```jsx
<Foo />
```
Do not pad JSX curly braces with spaces. 
```jsx
<Foo bar={baz} />
```
## Props
1. Always use camelCase for prop names.
```jsx
<Foo
  userName="hello"
  phoneNumber={12345678}
/>
```
2. Always include an alt prop on <img> tags. If the image is presentational, alt can be an empty string or the <img> must have role="presentation". eslint: jsx-a11y/alt-text
```jsx
// good
<img src="hello.jpg" alt="Me waving hello" />
// good
<img src="hello.jpg" alt="" />
// good
<img src="hello.jpg" role="presentation" />
```
3. Do not use words like "image", "photo", or "picture" in <img> alt props. eslint: jsx-a11y/img-redundant-alt
```jsx
// bad
<img src="hello.jpg" alt="Picture of me waving hello" />
// good
<img src="hello.jpg" alt="Me waving hello" />
```
4. Avoid using an array index as key prop, prefer a stable ID. eslint: react/no-array-index-key
```jsx
// bad
{todos.map((todo, index) =>
  <Todo
	{...todo}
	key={index}
  />
)}
// good
{todos.map(todo => (
  <Todo
    {...todo}
    key={todo.id}
  />
))}
``` 

5. Refs
Always use ref callbacks. eslint: react/no-string-refs
```jsx
// good
<Foo
  ref={(ref) => { this.myRef = ref; }}
/>
```
## Parentheses
wrap JSX tags in parentheses when they span more than one line. 
```jsx
// good
render() {
return (
<MyComponent variant="long body" foo="bar">
	<MyChild />
 </MyComponent>
);
}
// good, when single line
render() {
 const body = <div>hello</div>;
  return <MyComponent>{body}</MyComponent>;
}
```

## TAGS
Always self-close tags that have no children. eslint: react/self-closing-comp
```jsx
// good
<Foo variant="stuff" />
```

## Methods
Use arrow functions to close over local variables.
```jsx
function ItemList(props) {
  return (
    <ul>
      {props.items.map((item, index) => (
        <Item
          key={item.key}
          onClick={(event) => { doSomethingWith(event, item.name, index); }}
        />
      ))}
    </ul>
  );
}
```
## Bind event handlers using  public class fields syntax. 
```jsx
class extends React.Component {
  constructor(props) {
    super(props);
  }
  onClickDiv = () => {
    // do stuff
  }
  render() {
    return <div onClick={this.onClickDiv} />;
  }
}
```

## Be sure to return a value in your render methods. eslint: react/require-render-return
```jsx
// bad
render() {
  (<div />);
}
// good
render() {
  return (<div />);
```
## Comments
```jsx
Use // for single line comments.
Use /* ... / for multi-line comments.
```
## Strings that cause the line to go over 100 characters should not be written across multiple lines using string concatenation.
## Avoid single letter names. Be descriptive with your naming.
## Use the literal syntax for object and array creation (E.g.  var item = {};)
## Add spaces inside curly braces. (E.g. var foo = { clark: 'kent' };)
## Avoid spaces before commas and require a space after commas. (E.g. var arr = [1, 2])
## Avoid spaces between functions and their invocations.(E.g. var obj = {"foo": 42};)
## Ternaries should not be nested and generally be single line expressions. (E.g. var foo = maybe1 > maybe2 ? 'bar' : maybeNull;)

## Try to follow lifecycle ordering: 
```mermaid
graph TB
Optional static method --> Constructor --> componentDidMount --> shouldComponentUpdate --> componentDidUpdate --> componentWillUnmount --> render
```

### License

React is [MIT licensed](./LICENSE).
