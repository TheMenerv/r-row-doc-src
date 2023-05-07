---
id: Point
slug: point
---

The `Point` class represents a Point in 2D space.

<br/>

## Constructor

```ts title="prototype"
constructor(x: number, y: number, options: PointOptions = {})
```

### Properties

- `x`
  - Type: `number`
  - The x coordinate.

- `y`
  - Type: `number`
  - The y coordinate.

- `options` (optional)
  - Type: `PointOptions`
  - Default value: `{}`
  - The options for the Point

<br/>

## Methods

### setOptions

```ts title="prototype"
setOptions(options: PointOptions): Point
```

Set the options of the point.

#### Parameters

- `options`
  - Type: `PointOptions`
  - The point options.

#### Return

`Point` The point with the new options.

#### Example

```ts
const point = new Point(10, 10);
point.setOptions({ color: 'red', weight: 2 });
```

<br/>

### toArray

```ts title="prototype"
toArray(): [number, number]
```

Converts a point to an array.

#### Return

`[number, number]` Array with 2 numbers, the first is the x coordinate of the point and the second is the y coordinate of the point.

#### Example

```ts
const point = new Point(10, 10);
const arr = point.toArray();
```

<br/>

### add

```ts title="prototype"
add(point: Point): Point
```

Addition with another point.

#### Return

`Point` The result of the addition.

#### Example

```ts
const point1 = new Point(10, 10);
const point2 = new Point(10, 10);
const result = point1.add(point2);
```

<br/>

### subtract

```ts title="prototype"
subtract(point: Point): Point
```

Subtraction with another point.

#### Return

`Point` The result of the subtraction.

#### Example

```ts
const point1 = new Point(10, 10);
const point2 = new Point(10, 10);
const result = point1.subtract(point2);
```

<br/>

### multiply

```ts title="prototype"
multiply(point: Point): Point
```

Multiplication with another point.

#### Return

`Point` The result of the multiplication.

#### Example

```ts
const point1 = new Point(10, 10);
const point2 = new Point(10, 10);
const result = point1.multiply(point2);
```

<br/>

### divide

```ts title="prototype"
divide(point: Point): Point
```

Division with another point.

#### Return

`Point` The result of the division.

#### Example

```ts
const point1 = new Point(10, 10);
const point2 = new Point(10, 10);
const result = point1.divide(point2);
```

<br/>

### equals

```ts title="prototype"
equals(point: Point): boolean
```

Checks if the point is equal to another point.

#### Parameters

- `point`
  - Type: `Point`
  - The point to compare with

#### Return

`boolean` Whether the points are equal.

#### Example

```ts
const point1 = new Point(10, 10);
const point2 = new Point(10, 10);
const result = point1.equals(point2);
```

<br/>

### getDistanceWithPoint

```ts title="prototype"
getDistanceWithPoint(point: Point): number
```

Get the distance between two points.

#### Parameters

- `point`
  - Type: `Point`
  - The point to calculate the distance to.

#### Return

`number` The distance between the two points.

#### Example

```ts
const point1 = new Point(10, 10);
const point2 = new Point(20, 20);
const result = point1.getDistanceWithPoint(point2);
```

<br/>

### isOnLine

```ts title="prototype"
isOnLine(line: Line, tolerance: number = 0.1): boolean
```

Check if the point is on a line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to check.

- `tolerance` (optional)
  - Type: `number`
  - Default value: `0.1`
  - The tolerance of the check

#### Return

`boolean` Whether the point is on the line.

#### Example

```ts
const point = new Point(10, 10);
const line = new Line(new Point(0, 0), new Point(20, 20));
const result = point.isOnLine(line);
```

<br/>

### isOnRectangle

```ts title="prototype"
isOnRectangle(rectangle: Rectangle): boolean
```

Check if the point is on a rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`boolean` Whether the point is on the rectangle.

#### Example

```ts
const point = new Point(10, 10);
const rectangle = new Rectangle(new Point(0, 0), new Point(20, 20));
const result = point.isOnRectangle(rectangle);
```

<br/>

### isInRectangle

```ts title="prototype"
isInRectangle(rectangle: Rectangle): boolean
```

Check if the point is in a rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`boolean` Whether the point is in the rectangle.

#### Example

```ts
const point = new Point(10, 10);
const rectangle = new Rectangle(new Point(0, 0), new Point(20, 20));
const result = point.isInRectangle(rectangle);
```

<br/>

### isOnCircle

```ts title="prototype"
isOnCircle(circle: Circle, tolerance: number = 0.1): Point[]
```

Check if the point is on a circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

- `tolerance`
  - Type: `number`
  - Default value: `0.1`
  - The tolerance of the check.

#### Return

`boolean` Whether the point is on the circle.

#### Example

```ts
const point = new Point(10, 10);
const circle = new Circle(new Point(0, 0), 10);
const result = point.isOnCircle(circle);
```

<br/>

### isInCircle

```ts title="prototype"
isInCircle(circle: Circle, tolerance: number = 0.1): boolean
```

Check if the point is in a circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

- `tolerance`
  - Type: `number`
  - Default value: `0.1`
  - The tolerance of the check.

#### Return

`boolean` Whether the point is in the circle.

#### Example

```ts
const point = new Point(10, 10);
const circle = new Circle(new Point(0, 0), 10);
const result = point.isInCircle(circle);
```

<br/>

### clone

```ts title="prototype"
clone(): Point
```

Get a copy of point.

#### Return

`Point` The copy.

#### Example

```ts
const point = new Point(10, 10);
const copy = point.clone();
```

<br/>

### draw

```ts title="prototype"
draw(ctx: CanvasRenderingContext2D): void
```

Draw the Point.

#### Parameters

- `ctx`
  - Type: `CanvasRenderingContext2D`
  - The canvas context.

#### Return

`void`

#### Example

```ts
const point = new Point(10, 10);
point.draw(ctx);
```

<br/>

## Static methods

### fromArray

```ts title="prototype"
static fromArray(array: [number, number]): Point
```

Creates a point from an array

#### Parameters

- `array`
  - Type: `[number number]`
  - Array with 2 numbers, the first is x coordinate of the point and the second is the y coordinate of the point.

#### Return

`Point` The point.

#### Example

```ts
const point = Point.fromArray([10, 10]);
```