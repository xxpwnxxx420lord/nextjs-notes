comments are a  essential part of writing code as they help to describe the purpose of code every single coding language I know of has comments for example;

python:

```python
# comments
```

lua:

```lua
-- comment
```

but we aren’t learning python/lua or any of those goofy languages that doesn’t allow web application development, we are learning ts (for next.js) 

## Single comments

In coding, there's a type of comment called a `single line comment`. As the name suggests, it's a comment that takes up just one line. Here's how to use it.

```tsx
// This is a single-line comment
const greeting = "Hello, world!" // this makes a varible called "greeting" and sets the value to "Hello, World!"
console.log(greeting)// this prints out in the website console, (located in inspect element/development tools) the greeting value
```

## Muti-Line comments

when you code you might want to do a ASCII heading which is a heading which has art or you want to do a long explanation but don't want to keep typing the double slashes; this is the comment type you want to use.

```tsx
/*
the
quick
brown
fox
jumps
over
the
lazy
dog
/*
```

also this is a example of ascii art for those curious.

```tsx
/*
                                                              _____ _______________  .__                   .___
___  ______  ___________  _  ______ ___  ______  ______  ___ /  |  |\_____  \   _  \ |  |   ___________  __| _/
\  \/  /\  \/  /\____ \ \/ \/ /    \\  \/  /\  \/  /\  \/  //   |  |_/  ____/  /_\  \|  |  /  _ \_  __ \/ __ | 
 >    <  >    < |  |_> >     /   |  \>    <  >    <  >    </    ^   /       \  \_/   \  |_(  <_> )  | \/ /_/ | 
/__/\_ \/__/\_ \|   __/ \/\_/|___|  /__/\_ \/__/\_ \/__/\_ \____   |\_______ \_____  /____/\____/|__|  \____ | 
      \/      \/|__|              \/      \/      \/      \/    |__|        \/     \/                       \/ 
/*
```

## documentation comments

These comments are used to generate documentation and are typically used with functions, classes, and interfaces. They start with **`/**`** and end with **`/`**. You can use tags like **`@param`**, **`@returns`**, and **`@example`** to provide structured information.

```tsx
/**
 * Calculates the area of a circle.
 * @param radius - The radius of the circle.
 * @returns The area of the circle.
 * @example
 * const area = calculateCircleArea(5);
 * console.log(area); // Outputs: 78.53981633974483
 */
function calculateCircleArea(radius: number): number {
    return Math.PI * radius * radius;
}
```
