---
id: Touch
slug: touch
---

The `Touch` class is a singleton class that handles touch input.

:::info
Prefer to get the unique instance of this service from the `ServiceContainer` like:

```ts
const touch = ServiceContainer.touch;
```
:::

<br/>

## Getters

### instance

- Type: `Touch`

Get the instance of touch service.

### position

- Type: `Point`

Get the position of the touch on the canvas.

### isStarted

- Type: `boolean`

Touch has started.

### isMoved

- Type: `boolean`

Touch has moved.

### isEnded

- Type: `boolean`

Touch has ended.

### isCancelled

- Type: `boolean`

Touch has been cancelled.

### isDown

- Type: `boolean`

Touch is down.

### isUp

- Type: `boolean`

Touch is up.

### isClicked

- Type: `boolean`

Touch is clicked.

### isTouchScreen

- Type: `boolean`

Check if the device is a touch screen.

<br/>

## Methods

### setClickDelay

```ts title="prototype"
setClickDelay(delay: number): void
```

Set the delay for click events.

:::note
If delay was not set, his value is `0.3` second.
:::

#### Parameters

- `delay`
  - Type: `number`
  - The click delay.

#### Return

`void`

#### Example

```ts
ServiceContainer.Touch.setClickDelay(0.5);
```