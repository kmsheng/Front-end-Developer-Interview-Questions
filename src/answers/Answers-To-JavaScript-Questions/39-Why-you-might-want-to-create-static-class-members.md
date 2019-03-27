# Why you might want to create static class members ?
Because sometimes I want to use a class function without creating an instance, so I create a static class function instead.

For example
```js
class User {

  static list() {
    // fetch db here
  }
}

User.list();
```

Common shared properties can be defined as below
```js
class Greeting extends React.Component {

  render() {
    return (
      <div>Hello, {this.props.name}</div>
    )
  }
}

Greeting.defaultProps = {
  name: 'stranger'
};
```

### References
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/static
 - https://reactjs.org/docs/typechecking-with-proptypes.html
