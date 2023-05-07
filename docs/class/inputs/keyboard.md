---
id: Keyboard
slug: keyboard
---

The `Keyboard` class is a singleton class that handles keyboard input.

:::info
Prefer to get the unique instance of this service from the `ServiceContainer` like:

```ts
const keyboard = ServiceContainer.keyboard;
```
:::

<br/>

## Getters

### instance

- Type: `Keyboard`

Get the instance of keyboard service.

<br/>

## Methods

### isDown

```ts title="prototype"
isDown(key: string): boolean;
```

Check if a key is down.

#### Parameters

- `key`
  - Type: `string`
  - The key to check (it's an `event.code` from `KeyboardEvent`).

#### Return

`boolean` - `true` if the key is down, `false` otherwise.

#### Example

```ts
ServiceContainer.Keyboard.isDown('KeyA');
```

<br/>

### isUp

```ts title="prototype"
isUp(key: string): boolean;
```

Check if a key is up.

#### Parameters

- `key`
  - Type: `string`
  - The key to check (it's an `event.code` from `KeyboardEvent`).

#### Return

`boolean` - `true` if the key is up, `false` otherwise.

#### Example

```ts
ServiceContainer.Keyboard.isUp('KeyA');
```

<br/>

### isJustDown

```ts title="prototype"
isJustDown(key: string): boolean;
```

Check if a key is just down during the current frame.

#### Parameters

- `key`
  - Type: `string`
  - The key to check (it's an `event.code` from `KeyboardEvent`).

#### Return

`boolean` - `true` if the key is just down down, `false` otherwise.

#### Example

```ts
ServiceContainer.Keyboard.isJustDown('KeyA');
```

<br/>

### isJustUp

```ts title="prototype"
isJustUp(key: string): boolean;
```

Check if a key is just up during the current frame.

#### Parameters

- `key`
  - Type: `string`
  - The key to check (it's an `event.code` from `KeyboardEvent`).

#### Return

`boolean` - `true` if the key is just up, `false` otherwise.

#### Example

```ts
ServiceContainer.Keyboard.isJustUp('KeyA');
```