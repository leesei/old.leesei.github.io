title: "ReactJS"
date: 2015-02-09 14:55:43
categories:
- web
tags:
- react-js
- javascript
toc: true
---

```javascript
var HelloMessage = React.createClass({
  render: function() {
    return React.DOM.div(
                         {className: 'mystyle'},
                         'Hello ' + this.props.name
                         );
  }
});

React.renderComponent(HelloMessage({name:"John"}), mountNode);
```


```jsx
/** @jsx React.DOM */
var HelloMessage = React.createClass({
  render: function() {
    return <div>{'Hello ' + this.props.name}</div>;
  }
});

React.renderComponent(<HelloMessage name="John" />, mountNode);
```

[Tutorial | React](http://facebook.github.io/react/docs/tutorial.html)
[React JS Todo 2 - JSFiddle](http://jsfiddle.net/johnthethird/NXCyC/9/)
