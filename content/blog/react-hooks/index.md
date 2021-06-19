---
title: React Hooks
date: "2021-06-19T17:40:32.169Z"
description: React Hooks detail information with example
---

React one of the important and most used Frontend Framework in the web
development for past few years.

## React Class based component

In the earlier version of the react, `Class` Based component was used. The downside
of this approach was the initial boilerplate of code was way to much bigger, and debug
was harder. Now days React Class based component is totally outdated and nobody uses it
in the newer projects.

```jsx
class Button extends React.Component {
  constructor(props) {
    super(props);
    this.state = {

    }; // States for the component
  }

  render() {
    return (
      <button>Too much Code</button>
    )
  }
}

```

## React Function component

Functional component has way to much less initial codebase compared to class and is also more
readable.

```jsx
const Button = (props) => (<button>Hurray!!!</button>)

```

## React Hooks

Hooks are regular function specific to react that provide component functionality based on the
use-case. Hooks can be used as life-cycle methods or custom-hooks have custom logic.
Some of the most common hooks that are used in react

- **useState** Create the state and update state function
- **useEffect** Lifecycle method can we defined for `mount`, `update` and `unmount`
- **useRef** To get the reference of the node or current node state.


### React Custom Hooks

If one needs to create his/her own custom hooks it needs to start with `use` in the
function name.

```jsx
const useDateToAdd = (value) => {

  const updatedValue = useMemo(() => {
    // Some computation
    return value + 2;
  }, [value]);

  return updatedValue;

}

```

