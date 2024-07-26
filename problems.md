# Practice Problems


## For Loops

Question 1: Write a `for` loop that prints numbers from 1 to 5.

<details>
    <summary>Solution</summary>

```typescript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```
</details>

Question 2: Write a `for` loop that iterates over an array of numbers `[1, 2, 3, 4, 5]` and logs each number.

<details>
    <summary>Solution</summary>

```typescript
const numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);
}
```
</details>

## Foreach Loops

Question 1: Use `forEach` to log each element of the array `[1, 2, 3, 4, 5]`.

<details>
    <summary>Solution</summary>

```typescript
const numbers = [1, 2, 3, 4, 5];
numbers.forEach(number => console.log(number));
```
</details>

Question 2: Use `forEach` to log each element of the array `['a', 'b', 'c']` and its index.

<details>
    <summary>Solution</summary>

```typescript
const letters = ['a', 'b', 'c'];
letters.forEach((letter, index) => console.log(`${index}: ${letter}`));
```
</details>

## Iterating Over Objects

Question 1: Write a `for...in` loop to log each key and value of the object `{a: 1, b: 2, c: 3}`.

<details>
    <summary>Solution</summary>

```typescript
const obj = {a: 1, b: 2, c: 3};
for (let key in obj) {
    console.log(`${key}: ${obj[key]}`);
}
```
</details>

Question 2: Use `Object.keys` to iterate over the keys of the object `{x: 10, y: 20}` and log each key.

<details>
    <summary>Solution</summary>

```typescript
const obj = {x: 10, y: 20};
Object.keys(obj).forEach(key => console.log(key));
```
</details>

## Map

Question 1: Use `map` to create a new array with each element of `[1, 2, 3]` doubled.

<details>
    <summary>Solution</summary>

```typescript
const numbers = [1, 2, 3];
const doubled = numbers.map(n => n * 2);
console.log(doubled); // [2, 4, 6]
```
</details>

Question 2: Use `map` to convert an array of strings `['1', '2', '3']` to numbers.

<details>
    <summary>Solution</summary>

```typescript
const strings = ['1', '2', '3'];
const numbers = strings.map(s => parseInt(s));
console.log(numbers); // [1, 2, 3]
```
</details>

## Filter

Question 1: Use `filter` to create a new array with only the even numbers from `[1, 2, 3, 4, 5]`.

<details>
    <summary>Solution</summary>

```typescript
const numbers = [1, 2, 3, 4, 5];
const evens = numbers.filter(n => n % 2 === 0);
console.log(evens); // [2, 4]
```
</details>

Question 2: Use `filter` to create a new array with only the strings longer than 3 characters from `['apple', 'cat', 'dog']`.

<details>
    <summary>Solution</summary>

```typescript
const strings = ['apple', 'cat', 'dog'];
const longStrings = strings.filter(s => s.length > 3);
console.log(longStrings); // ['apple']
```
</details>

## Find

Question 1: Use `find` to locate the first even number in the array `[1, 3, 4, 6]`.

<details>
    <summary>Solution</summary>

```typescript
const numbers = [1, 3, 4, 6];
const firstEven = numbers.find(n => n % 2 === 0);
console.log(firstEven); // 4
```
</details>

Question 2: Use `find` to locate the first string with more than 3 characters in the array `['a', 'ab', 'abc', 'abcd']`.

<details>
    <summary>Solution</summary>

```typescript
const strings = ['a', 'ab', 'abc', 'abcd'];
const firstLong = strings.find(s => s.length > 3);
console.log(firstLong); // 'abcd'
```
</details>

## Functions

Question 1: Write a function that adds two numbers and returns the result.

<details>
    <summary>Solution</summary>

```typescript
function add(a: number, b: number): number {
    return a + b;
}
console.log(add(2, 3)); // 5
```
</details>

Question 2: Write a function that takes a string and returns it in uppercase.

<details>
    <summary>Solution</summary>

```typescript
function toUpperCase(str: string): string {
    return str.toUpperCase();
}
console.log(toUpperCase('hello')); // 'HELLO'
```
</details>

## Hooks

Question 1: Create a component that uses `useState` to manage a counter.

<details>
    <summary>Solution</summary>

```typescript
import React, { useState } from 'react';

const Counter: React.FC = () => {
    const [count, setCount] = useState(0);

    return (
        <div>
            <p>{count}</p>
            <button onClick={() => setCount(count + 1)}>Increment</button>
        </div>
    );
};
```
</details>

Question 2: Create a component that uses `useState` to manage a text input value.

<details>
    <summary>Solution</summary>

```typescript
import React, { useState } from 'react';

const TextInput: React.FC = () => {
    const [value, setValue] = useState('');

    return (
        <div>
            <input value={value} onChange={e => setValue(e.target.value)} />
            <p>{value}</p>
        </div>
    );
};
```
</details>

Question 1: Use `useEffect` to log a message when the component mounts.

<details>
    <summary>Solution</summary>

```typescript
import React, { useEffect } from 'react';

const Logger: React.FC = () => {
    useEffect(() => {
        console.log('Component mounted');
    }, []);

    return <div>Check the console</div>;
};
```
</details>

Question 2: Use `useEffect` to update the document title when the count state changes.

<details>
    <summary>Solution</summary>

```typescript
import React, { useState, useEffect } from 'react';

const TitleUpdater: React.FC = () => {
    const [count, setCount] = useState(0);

    useEffect(() => {
        document.title = `Count: ${count}`;
    }, [count]);

    return (
        <div>
            <p>{count}</p>
            <button onClick={() => setCount(count + 1)}>Increment</button>
        </div>
    );
};
```
</details>

## Events

Question 1: Create a button that logs "Button clicked" to the console when clicked.

<details>
    <summary>Solution</summary>

```typescript
import React from 'react';

const ClickButton: React.FC = () => {
    const handleClick = () => {
        console.log('Button clicked');
    };

    return <button onClick={handleClick}>Click me</button>;
};
```
</details>

Question 2: Create an input field that logs its value to the console when it changes.

<details>
    <summary>Solution</summary>

```typescript
import React from 'react';

const InputLogger: React.FC = () => {
    const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
        console.log(e.target.value);
    };

    return <input onChange={handleChange} />;
};
```
</details>

## Callbacks

Question 1: Write a function that takes a callback and calls it with the value 5.

<details>
    <summary>Solution</summary>

```typescript
function withCallback(callback: (num: number) => void): void {
    callback(5);
}

withCallback(console.log); // Logs: 5
```
</details>

Question 2: Write a function that takes a callback and a string, and calls the callback with the uppercase version of the string.

<details>
    <summary>Solution</summary>

```typescript
function processString(str: string, callback: (s: string) => void): void {
    callback(str.toUpperCase());
}

processString('hello', console.log); // Logs: 'HELLO'
```
</details>

## Switch Statements

Question 1: Write a `switch` statement that logs the name of the day for a given number (1-7).

<details>
    <summary>Solution</summary>

```typescript
const dayNumber = 3;
switch (dayNumber) {
    case 1: console.log('Monday'); break;
    case 2: console.log('Tuesday'); break;
    case 3: console.log('Wednesday'); break;
    case 4: console.log('Thursday'); break;
    case 5: console.log('Friday'); break;
    case 6: console.log('Saturday'); break;
    case 7: console.log('Sunday'); break;
    default: console.log('Invalid day'); break;
}
```
</details>

Question 2: Write a `switch` statement that logs a message based on the status code (200, 404, 500).

<details>
    <summary>Solution</summary>

```typescript
const statusCode = 404;
switch (statusCode) {
    case 200: console.log('OK'); break;
    case 404: console.log('Not Found'); break;
    case 500: console.log('Internal Server Error'); break;
    default: console.log('Unknown status'); break;
}
```
</details>

## Ternary

Question 1: Use a ternary operator to log "Even" or "Odd" based on a number.

<details>
    <summary>Solution</summary>

```typescript
const num = 4;
console.log(num % 2 === 0 ? 'Even' : 'Odd'); // Logs: 'Even'
```

Question 2: Use a ternary operator to assign a message based on the age being greater than or equal to 18.

```typescript
const age = 20;
const message = age >= 18 ? 'Adult' : 'Minor';
console.log(message); // Logs: 'Adult'
```
</details>

## Types

Question 1: Define a type alias for a function that takes a number and returns a string.

<details>
    <summary>Solution</summary>

```typescript
type NumberToString = (num: number) => string;

const numToString: NumberToString = (num) => num.toString();
console.log(numToString(5)); // '5'
```
</details>

Question 2: Define a type alias for an object with name (string) and age (number).

<details>
    <summary>Solution</summary>

```typescript
type Person = {
    name: string;
    age: number;
};

const person: Person = { name: 'Alice', age: 30 };
console.log(person);
```
</details>

## Type Inference

Question 1: Declare a variable with an initial value and let TypeScript infer its type.

<details>
    <summary>Solution</summary>

```typescript
const count = 10; // TypeScript infers 'number'
console.log(typeof count); // 'number'
```
</details>

Question 2: Write a function with inferred return type based on its return value.

<details>
    <summary>Solution</summary>

```typescript
function add(a: number, b: number) {
    return a + b; // TypeScript infers 'number' return type
}

console.log(add(2, 3)); // 5
```
</details>

## Custom Types

Question 1: Define a custom type for a function that takes a string and returns a boolean.

<details>
    <summary>Solution</summary>

```typescript
type StringToBoolean = (str: string) => boolean;

const isStringEmpty: StringToBoolean = (str) => str.length === 0;
console.log(isStringEmpty('')); // true
```
</details>

Question 2: Define a custom type for an object with a title (string) and completed (boolean).

<details>
    <summary>Solution</summary>

```typescript
type Task = {
    title: string;
    completed: boolean;
};

const task: Task = { title: 'Learn TypeScript', completed: false };
console.log(task);
```
</details>

## Interfaces

Question 1: Define an interface for a user object with id (number) and name (string).

<details>
    <summary>Solution</summary>

```typescript
interface User {
    id: number;
    name: string;
}

const user: User = { id: 1, name: 'John Doe' };
console.log(user);
```
</details>

Question 2: Define an interface for a function that takes two numbers and returns a number.

<details>
    <summary>Solution</summary>

```typescript
interface AddFunction {
    (a: number, b: number): number;
}

const add: AddFunction = (a, b) => a + b;
console.log(add(2, 3)); // 5
```
</details>

## Props in TypeScript

Question 1: Define a component that takes a name prop (string) and displays it.

<details>
    <summary>Solution</summary>

```typescript
import React from 'react';

type Props = {
    name: string;
};

const Greeting: React.FC<Props> = ({ name }) => {
    return <h1>Hello, {name}!</h1>;
};
```
</details>

Question 2: Define a component that takes a count prop (number) and displays it.

<details>
    <summary>Solution</summary>

```typescript
import React from 'react';

type Props = {
    count: number;
};

const Counter: React.FC<Props> = ({ count }) => {
    return <p>Count: {count}</p>;
};
```
</details>

## Rest Parameters

Question 1: Write a function that takes any number of arguments and logs them.

<details>
    <summary>Solution</summary>

```typescript
function logAll(...args: any[]): void {
    console.log(args);
}

logAll(1, 'a', true); // [1, 'a', true]
```
</details>

Question 2: Write a function that takes a first argument and rest arguments, and logs them.

<details>
    <summary>Solution</summary>

```typescript
function logFirstAndRest(first: any, ...rest: any[]): void {
    console.log(first, rest);
}

logFirstAndRest(1, 'a', true); // 1 ['a', true]
```
</details>

## Spread Syntax

Question 1: Use spread syntax to combine two arrays [1, 2] and [3, 4].

<details>
    <summary>Solution</summary>

```typescript
const array1 = [1, 2];
const array2 = [3, 4];
const combined = [...array1, ...array2];
console.log(combined); // [1, 2, 3, 4]
```
</details>

Question 2: Use spread syntax to create a new object with additional properties.

<details>
    <summary>Solution</summary>

```typescript
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 };
console.log(obj2); // { a: 1, b: 2, c: 3 }
```
</details>

## Objects

Question 1: Create an object with properties name (string) and age (number).

<details>
    <summary>Solution</summary>

```typescript
const person = {
    name: 'Alice',
    age: 30
};
console.log(person);
```
</details>

Question 2: Access the properties name and age of an object `{ name: 'Bob', age: 25 }`.

<details>
    <summary>Solution</summary>

```typescript
const person = {
    name: 'Bob',
    age: 25
};
console.log(person.name); // 'Bob'
console.log(person.age);  // 25
```
</details>

## Array Destructuring

Question 1: Use array destructuring to extract the first two elements of `[1, 2, 3]`.

<details>
    <summary>Solution</summary>

```typescript
const array = [1, 2, 3];
const [first, second] = array;
console.log(first, second); // 1 2
```
</details>

Question 2: Use array destructuring to swap the values of `a` and `b`.

<details>
    <summary>Solution</summary>

```typescript
let a = 1;
let b = 2;
[a, b] = [b, a];
console.log(a, b); // 2 1
```
</details>

## Object Destructuring

Question 1: Use object destructuring to extract name and age from `{ name: 'Charlie', age: 28 }`.

<details>
    <summary>Solution</summary>

```typescript
const person = { name: 'Charlie', age: 28 };
const { name, age } = person;
console.log(name, age); // 'Charlie' 28
```
</details>

Question 2: Use object destructuring to extract title with a default value from `{ title: 'Book' }`.

<details>
    <summary>Solution</summary>

```typescript
const item = { title: 'Book' };
const { title, author = 'Unknown' } = item;
console.log(title, author); // 'Book' 'Unknown'
```
</details>

## Enums

Question 1: Define an enum for days of the week and log the value for Wednesday.

<details>
    <summary>Solution</summary>

```typescript
enum Days {
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
}
console.log(Days.Wednesday); // 2
```
</details>

Question 2: Define an enum for colors and log the value for Red.

<details>
    <summary>Solution</summary>

```typescript
enum Colors {
    Red = 'RED',
    Green = 'GREEN',
    Blue = 'BLUE'
}
console.log(Colors.Red); // 'RED'
```
</details>

## Generics

Question 1: Write a generic function that takes an array and returns its first element.

<details>
    <summary>Solution</summary>

```typescript
function getFirstElement<T>(arr: T[]): T {
    return arr[0];
}
console.log(getFirstElement([1, 2, 3])); // 1
```
</details>

Question 2: Write a generic function that takes a value and returns it as an array.

<details>
    <summary>Solution</summary>

```typescript
function toArray<T>(value: T): T[] {
    return [value];
}
console.log(toArray(5)); // [5]
```
</details>
