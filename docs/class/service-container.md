---
id: ServiceContainer
slug: service-container
---

The `ServiceContainer` class is a container for various services used in the game. It provides a convenient way to access singleton instances of these services.

:::info
It is possible to use the different services by calling the `instance` getters rather than the `ServiceContainer`. However, the objective of this class is to facilitate access to these services and make the code more readable.
:::

<br/>

## Properties

### AssetStore

The instance of the `AssetStore` class.

### GameCanvas

The instance of the `GameCanvas` class.

### GameLoop

The instance of the `GameLoop` class.

### Keyboard

The instance of the `Keyboard` class.

### Mouse

The instance of the `Mouse` class.

### SceneManager

The instance of the `SceneManager` class.

### Touch

The instance of the `Touch` class.