# Class Components

## Typing Props

Given the following component,

```javascript
class Hello extends React.Component {
  render() {
    return <div className="message-box">Hello {this.props.name}</div>;
  }
}
```

type the prop like this:

```typescript
class Hello extends React.Component<{ name: string }> {
  // Notice render method is public
  public render() {
    return <div className="message-box">Hello {this.props.name}</div>;
  }
}
```

## Typing State

Given the following component,

```javascript
class Hello extends React.Component {
  state = {
    open: false;
  }

  render() {
    return state.open ? <div className="message-box">Hello</div> : null;
  }
}
```

type the state like this:

```typescript
interface State {
  open: boolean;
}

class Hello extends React.Component<{}, State> {
  // Notice state is public
  public state: State = {
    open: false;
  }

  public render() {
    return state.open ? <div className="message-box">Hello</div> : null;
  }
}
```
