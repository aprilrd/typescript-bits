# Event Handler

Each DOM event has a corresponding `Handler` type: `React.KeyboardEventHandler` and
`React.MouseEventHandler` are such examples. To type an event callback, do this:

```typescript
function Hello({
  onClick
}: {
  onClick: React.MouseEventHandler<HTMLDivElement>;
}) {
  return <div onClick={onClick}>Hello</div>;
}
```
