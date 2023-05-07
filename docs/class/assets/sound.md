---
id: Sound
slug: sound
---

The `Sound` class represents a sound and provides methods to play, pause, stop, and manipulate its properties.

<br/>

## Constructor

```ts title="prototype"
constructor(name: string, loop: boolean = false);
```

### Properties

- `name`
  - Type: `string`
  - The name of the sound (on `AssetStore.images`)

- `loop` (optional)
  - Type: `boolean`
  - Default value: `false`
  - Whether or not the sound should loop.

<br/>

## Getters

### name

- Type: `string`

Returns the name of the sound.

### isPlaying

- Type: `boolean`

Returns whether or not the sound is playing.

### isPaused

- Type: `boolean`

Returns whether or not the sound is paused.

### isStopped

- Type: `boolean`

Returns whether or not the sound is stopped.

### duration

- Type: `number`

Returns the duration of the sound.

<br/>

## Getters & Setters

### volume

- Type: `number`

Gets and sets the volume of the sound (between 0 and 1).

### muted

- Type: `boolean`

Gets and sets whether or not the sound is muted.

### loop

- Type: `boolean`

Gets and sets whether or not the sound is looping.

### currentTime

- Type: `number`

Gets and sets the current time of the sound.

<br/>

## Methods

### play

```ts title="prototype"
play(): Sound;
```

Plays the sound and returns it.

#### Return

`Sound` The sound.

#### Example

```ts
const sound = new Sound('mySound');
sound.play();
```

<br/>

### pause

```ts title="prototype"
pause(): Sound;
```

Pauses the sound and returns it.

#### Return

`Sound` The sound.

#### Example

```ts
const sound = new Sound('mySound');
sound.play();
//...
sound.pause();
```

<br/>

### stop

```ts title="prototype"
stop(): Sound;
```

Stops the sound and returns it.

#### Return

`Sound` The sound.

#### Example

```ts
const sound = new Sound('mySound');
sound.play();
//...
sound.stop();
```