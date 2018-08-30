Components
======

Components can do two things:

1. Render UI from a data model

    We have already seen this with the hello world example:

    ```html
    const HelloWorld = (props) =>
    <div>Hello {props.name}</div>;

    <HelloWorld name="Ernesto" />
    ```

    Fork the [Circle rendering exercise](https://codepen.io/liammclennan/pen/EeyKEj?editors=0010) and complete it.

1. Publish data as events.

    ```html
    <HelloWorld name="Ernesto" onSomething={(data) => { console.log(data); } } />
    ```

    Review the [Publishing data example](https://codepen.io/liammclennan/pen/RYRamx?editors=0010)

Class syntax
------------

There is an alternative syntax for specifying components. It is not as good, so you should not use it unless you have to. 

```javascript
class HelloWorld extends React.Component {
    constructor(props) {
        super(props);
    }

    render() {
        return <div>Hello {props.name}</div>
    }
}
```