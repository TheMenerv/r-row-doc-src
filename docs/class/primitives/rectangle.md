---
id: Rectangle
slug: rectangle
---

The `Rectangle` class represents a Rectangle in 2D space.

<br/>

## Constructor

```ts title="prototype"
constructor(position: Point, size: Point, options: RectangleOptions = {})
```

### Properties

- `position`
  - Type: `Point`
  - The top left position of the rectangle.

- `size`
  - Type: `Point`
  - The size of the rectangle.

- `options` (optional)
  - Type: `RectangleOptions`
  - Default value: `{}`
  - The options for the rectangle.

<br/>

## Getters

### top

- Type: `number`

The top position of the rectangle.

### bottom

- Type: `number`

The bottom position of the rectangle.

### left

- Type: `number`

The left position of the rectangle.

### right

- Type: `number`

The right position of the rectangle.

### topLeft

- Type: `Point`

The topLeft point of the rectangle.

### topRight

- Type: `Point`

The topRight point of the rectangle.

### bottomLeft

- Type: `Point`

The bottomLeft point of the rectangle.

### bottomRight

- Type: `Point`

The bottomRight point of the rectangle.

### topLine

- Type: `Line`

The topLine line of the rectangle.

### rightLine

- Type: `Line`

The rightLine line of the rectangle.

### bottomLine

- Type: `Line`

The bottomLine line of the rectangle.

### leftLine

- Type: `Line`

The leftLine line of the rectangle.

<br/>

## Methods

### setOptions

```ts title="prototype"
setOptions(options: RectangleOptions): Circle
```

Set the options of the rectangle.

#### Parameters

- `options`
  - Type: `RectangleOptions`
  - The rectangle options.

#### Return

`Rectangle` The rectangle with the new options.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
rectangle.setOptions({ fillColor: 'red', weight: 2, strokeColor: 'blue', radius: 5 });
```

<br/>

### toArray

```ts title="prototype"
toArray(): [number, number, number, number]
```

Converts a rectangle to an array.

#### Return

`[number, number, number, number]` Array with 4 numbers, the two first are the top left position of the rectangle and the two remaining are the size of the line.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const array = rectangle.toArray();
```

<br/>

### equals

```ts title="prototype"
equals(rectangle: Rectangle): boolean
```

Check if the rectangle is equal to another rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to compare.

#### Return

`boolean` Whether the rectangle are equal.

#### Example

```ts
const rectangle1 = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangle2 = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangle3 = new Rectangle(new Point(10, 20), new Point(10, 10));
rectangle1.equals(rectangle2); // true
rectangle1.equals(rectangle3); // false
rectangle2.equals(rectangle3); // false
```

<br/>

### isContainsPoint

```ts title="prototype"
isContainsPoint(point: Point, tolerance: number = 0.1): boolean
```

Checks if the rectangle contains a point.

#### Parameters

- `point`
  - Type: `Point`
  - The point to check

- `tolerance` (optional)
  - Type: `number`
  - Default value: `0.1`
  - The tolerance to use

#### Return

`boolean` Whether the rectangle contains the point.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const point1 = new Point(10, 10);
const point2 = new Point(20, 20);
const point3 = new Point(30, 30);
rectangle.isContainsPoint(point1); // true
rectangle.isContainsPoint(point2); // true
rectangle.isContainsPoint(point3); // false
```

<br/>

### isIntersectsWithRectangle

```ts title="prototype"
isIntersectsWithRectangle(rectangle: Rectangle): boolean
```

Check if the rectangle intersects with another rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`boolean` Whether the rectangle intersect.

#### Example

```ts
const rectangle1 = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangle2 = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangle3 = new Rectangle(new Point(10, 20), new Point(10, 10));
rectangle1.isIntersectsWithRectangle(rectangle2); // true
rectangle1.isIntersectsWithRectangle(rectangle3); // false
rectangle2.isIntersectsWithRectangle(rectangle3); // false
```

<br/>

### getIntersectionsWithRectangle

```ts title="prototype"
getIntersectionsWithRectangle(rectangle: Rectangle): Point[]
```

Get the intersection of the rectangle with another rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`Point[]` The intersections.

#### Example

```ts
const rectangle1 = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangle2 = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangle3 = new Rectangle(new Point(10, 20), new Point(10, 10));
rectangle1.getIntersectionWithRectangle(rectangle2); // [Point(10, 10), Point(20, 10), Point(20, 20), Point(10, 20)]
rectangle1.getIntersectionWithRectangle(rectangle3); // []
rectangle2.getIntersectionWithRectangle(rectangle3); // []
```

<br/>

### isIntersectsWithLine

```ts title="prototype"
isIntersectsWithLine(line: Line): boolean
```

Check if the rectangle intersects with a line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to check.

#### Return

`boolean` Whether the line intersects with the rectangle.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const line1 = new Line(new Point(10, 10), new Point(20, 20));
const line2 = new Line(new Point(10, 20), new Point(20, 10));
const line3 = new Line(new Point(30, 30), new Point(40, 40));
rectangle.isIntersectsWithLine(line1); // true
rectangle.isIntersectsWithLine(line2); // true
rectangle.isIntersectsWithLine(line3); // false
```

<br/>

### getIntersectionsWithLine

```ts title="prototype"
getIntersectionsWithLine(line: Line): Point[]
```

Get the intersection of the rectangle with a line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to check.

#### Return

`Point[]` The intersection points.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const line1 = new Line(new Point(10, 10), new Point(20, 20));
const line2 = new Line(new Point(10, 20), new Point(20, 10));
const line3 = new Line(new Point(30, 30), new Point(40, 40));
rectangle.getIntersectionsWithLine(line1); // [Point(10, 10), Point(20, 20)]
rectangle.getIntersectionsWithLine(line2); // [Point(10, 20), Point(20, 10)]
rectangle.getIntersectionsWithLine(line3); // []
```

<br/>

### isIntersectsWithCircle

```ts title="prototype"
isIntersectsWithCircle(circle: Circle): boolean
```

Check if the rectangle intersects with a circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

#### Return

`boolean` Whether the circle is in the rectangle.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const circle1 = new Circle(new Point(10, 10), 10);
const circle2 = new Circle(new Point(20, 20), 10);
const circle3 = new Circle(new Point(30, 30), 10);
rectangle.isIntersectsWithCircle(circle1); // true
rectangle.isIntersectsWithCircle(circle2); // true
rectangle.isIntersectsWithCircle(circle3); // false
```

<br/>

### getIntersectionsWithCircle

```ts title="prototype"
getIntersectionsWithCircle(circle: Circle): Point[]
```

Check if the line intersects with a circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

#### Return

`Point[]` The intersection of the rectangle with a circle.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const circle1 = new Circle(new Point(10, 10), 10);
const circle2 = new Circle(new Point(20, 20), 10);
const circle3 = new Circle(new Point(30, 30), 10);
rectangle.getIntersectionsWithCircle(circle1); // [Point(10, 10), Point(20, 20)]
rectangle.getIntersectionsWithCircle(circle2); // [Point(10, 20), Point(20, 10)]
rectangle.getIntersectionsWithCircle(circle3); // []
```

<br/>

### clone

```ts title="prototype"
clone(): Rectangle
```

Get a copy of rectangle.

#### Return

`Rectangle` The copy.

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
const rectangleClone = rectangle.Clone();
```

<br/>

### draw

```ts title="prototype"
draw(ctx: CanvasRenderingContext2D): void
```

Draw the Rectangle.

#### Parameters

- `ctx`
  - Type: `CanvasRenderingContext2D`
  - The canvas context.

#### Return

`void`

#### Example

```ts
const rectangle = new Rectangle(new Point(10, 10), new Point(10, 10));
rectangle.draw(ctx);
```

<br/>

## Static methods

### fromArray

```ts title="prototype"
static fromArray(array: [number, number, number, number]): Rectangle
```

Creates a rectangle from an array

#### Parameters

- `array`
  - Type: `[number, number, number number]`
  - Array with 4 numbers, the two first are the top left position of the rectangle and the two remaining are the size of the line.

#### Return

`Rectangle` The rectangle.

#### Example

```ts
const rectangle = Rectangle.fromArray([10, 10, 10, 10]);
```