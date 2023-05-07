---
id: AssetStore
slug: asset-store
---

The `AssetStore` class is a singleton class that manages the storage and loading of various assets, such as sounds, images, and fonts.

<br/>

## Getters

### instance

- Type: `AssetStore`

Returns the instance of the AssetStore class.

### sounds

- Type: `Map<string, HTMLAudioElement>`

Returns the map of all the sounds.

### images

- Type: `Map<string, HTMLImageElement>`

Returns the map of all the images.

<br/>

## Methods

### addFont

```ts title="prototype"
addFont(name: string, url: string): AssetStore;
```

Adds a font to the `AssetStore`.

#### Parameters

- `name`
  - Type: `string`
  - The name of the font

- `url`
  - Type: `string`
  - The URL of the font

#### Return

`AssetStore` The instance of the AssetStore class.

#### Example

```ts
import myFontUrl from './fonts/myFont.ttf'
ServiceContainer.AssetStore.addSound('myFont', myFontUrl);
```

<br/>

### addImage

```ts title="prototype"
addImage(name: string, url: string): AssetStore;
```

Adds an image to the `AssetStore`.

#### Parameters

- `name`
  - Type: `string`
  - The name of the image

- `url`
  - Type: `string`
  - The URL of the image

#### Return

`AssetStore` The instance of the AssetStore class.

#### Example

```ts
import myImageUrl from './images/mySImage.png'
ServiceContainer.AssetStore.addImage('myImage', myImageUrl);
```

<br/>

### addSound

```ts title="prototype"
addSound(name: string, url: string): AssetStore;
```

Adds a sound to the `AssetStore`.

#### Parameters

- `name`
  - Type: `string`
  - The name of the sound

- `url`
  - Type: `string`
  - The URL of the sound

#### Return

`AssetStore` The instance of the AssetStore class.

#### Example

```ts
import mySoundUrl from './sounds/mySound.mp3'
ServiceContainer.AssetStore.addSound('mySound', mySoundUrl);
```

<br/>

### getSound

```ts title="prototype"
getSound(name: string): HTMLAudioElement;
```

Returns a sound from the `AssetStore`.

#### Parameters

- `name`
  - Type: `string`
  - The name of the sound

#### Return

`HTMLAudioElement` The sound.

#### Example

```ts
ServiceContainer.AssetStore.getSound('mySound');
```

<br/>

### getImage

```ts title="prototype"
getImage(name: string): HTMLImageElement;
```

Returns an image from the `AssetStore`.

#### Parameters

- `name`
  - Type: `string`
  - The name of the image

#### Return

`HTMLImageElement` The image.

#### Example

```ts
ServiceContainer.AssetStore.getImage('myImage');
```

<br/>

### loadAllAssets

```ts title="prototype"
loadAllAssets(): Promise<void[]>;
```

Loads all the assets and returns a promise that resolves when all the assets are loaded.

#### Return

`Promise<void[]>` The promise that resolves when all the assets are loaded.

#### Example

```ts
ServiceContainer.AssetStore.loadAllAssets();
```

## Complete usage example

```ts
import { ServiceContainer } from 'r-row';
// Fonts
import myFont from '../fonts/myFont.ttf';
// Images
import myImage from '../images/myImage.png';
// Sounds
import myImage from '../sounds/mySOund.wav';

ServiceContainer.AssetStore
  .addFont('myFont', myFont)
  .addImage('myImage', myImage)
  .addSound('mySound', mySound)
  .loadAllAssets()
  .then(() => {
    //...
  });
```