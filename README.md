# snabbdom-safe-props

Snabbdom replacement for default module 'props' with unsupported 'type' protection.
This simply adds a try/catch if the property being updated is `type`, as unsupported
types will cause the browser to throw an exception.

### Usage

Install:

`npm i snabbdom-safe-props --save`

Use:

```javascript
var patch = snabbdom.init([
  require('snabbdom-safe-props') // Instead of require('snabbdom/modules/props')
]);
```

### The props module

Allows you to set properties on DOM elements.

```javascript
h('a', {props: {href: '/foo'}}, 'Go to Foo');
```
