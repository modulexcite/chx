# chx

A wrapper on top of JSX to make outputting text on a terminal
with [chalk](https://github.com/chalk/chalk) a HTML-like experience.

## How to use

```js
/** @jsx chx */
import chx from 'chx';

console.log(<p>
  Welcome to the <b>future</b>.<br />
  What's your <cyan>name</cyan>?<br />
  Hope you enjoy your <bg color="yellow">time here</bg>.
</p>);
```

and make sure the babel transform [`react-jsx`](https://www.npmjs.com/package/babel-plugin-transform-react-jsx) is in place.

## Built ins

- All the colors, modifiers and bgColors from `chalk` are available as 
  tags. For example: `<bgRed>`, `<blue>` and `<italic`>
- The HTML shorthands are exposed when available:
  - `<b>` (bold)
  - `<i>` (italic)
  - `<u>` (underline)
  - `<strike>` (strikethrough)
- A special `<bg color>` element is available as a shorthand for 
- To wrap, we expose a few noop elements. Use whichever you like most:
  - `<p>`
  - `<chx>`
  - `<span>`

## Advanced UI

For more advanced UI needs,
check out [react-blessed](https://github.com/Yomguithereal/react-blessed).