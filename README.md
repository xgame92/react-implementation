# react-implementation

#### ES5 Class Component
```js
var HelloWorld = React.createClass({
    render:function(){
        <h1>Hello World</h1>
    };
});
```
#### ES5 Stateless Functional Component
```js
// ES5 Stateless Functional Component
..
var HelloWorld = function(props){
    return (
        <h1>Hello World</h1>
    );
});
```

#### React in ES6
- No Autobind
- PropTypes declared seperately
- Default props declared seperately
- Set initial state in constructor

```js
// Works fine with ES5 createClass
<div onClick={this.handleClick}></div>
```

```js
// Requires explicit bind with ES6 Class
<div onClick={this.handleClick.bind(this)}></div>
```

```js
// ES6 Class Component
class Contacts extends React.Component{
    contructor(props){
        super(props);
        this.handleClick = this.handleClick.bind(this);
    }
    ...
```

#### ES6 Stateless Functional Component
```js
// ES6 Stateless Functional Component 
..
// let or const but I use const because I dont want to HelloWorld function assigned accidently reassigned
const HelloWorld = (props) => {
    return (
        <h1>Hello World</h1>
    );
});
```



