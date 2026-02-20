# JS Computer Science Fundamentals

Exercises for the [Computer Science Fundamentals](https://www.learnjs.tech/js-comp-sci) lesson.

Work through this file top to bottom. Read the lesson section first, then complete the exercises here. Run your file after each section to check your output, then commit before moving on.

## Setup

```bash
bun install
```

## How to Run Your Work

All your code goes in `index.js`. Run it anytime with:

```bash
bun run index.js
```

You'll see the output of every `console.log` in your terminal.

---

## Exercise 1: Creating References

**Read first**: Memory Model and Binding Data to References sections of the lesson.

Open `index.js` and complete the following.

**Part A** — Declare a variable for each value below using the correct keyword (`const` or `let`). Log each one.

- Your name (won't change)
- Your current age (will change on your birthday)
- Whether you are currently a student (won't change this semester)

**Part B** — Reassignment and the heap. Write the following code, then answer the questions as comments directly below it:

```js
let city = "Chicago";
city = "St. Louis";
console.log(city);
```

- What gets logged?
- What happened to the string `"Chicago"` in memory?
- Why did we use `let` instead of `const` here?

**Part C** — Predict the output before running. Write your prediction as a comment on each line, then run to verify:

```js
let count = 1;
count = count + 1;
count = count + 1;
console.log(count); // Prediction:
```

**Commit when done**: `git add index.js` → `git commit -m "Complete references exercises"`

---

## Exercise 2: Types and typeof

**Read first**: Types and Type Checking sections of the lesson.

**Part A** — Before running, predict what `typeof` returns for each. Write your prediction as a comment, then uncomment to verify:

```js
// console.log(typeof "hello");     // Prediction:
// console.log(typeof 100);         // Prediction:
// console.log(typeof true);        // Prediction:
// console.log(typeof undefined);   // Prediction:
// console.log(typeof null);        // Prediction: (⚠️ watch out)
```

**Part B** — Dynamic typing in action. Run this and explain what it demonstrates in a comment:

```js
let age = 30;
console.log(typeof age);

age = "thirty";
console.log(typeof age);

// What does this tell you about how JavaScript handles types?
// Answer:
```

**Commit when done**: `git commit -m "Complete types and typeof exercises"`

---

## Exercise 3: Immutability

**Read first**: Immutability Deep Dive section of the lesson.

Run the code below and answer the questions as comments:

```js
let greeting = "Hello";
const original = greeting;

greeting = greeting + ", World!";

console.log(greeting);  // What logs here?
console.log(original);  // What logs here? Why is it different?

// Did the string "Hello" change, or was a new string created?
// Answer:

// Why does `original` still hold "Hello"? Explain using references.
// Answer:
```

**Commit when done**: `git commit -m "Complete immutability exercises"`

---

## Exercise 4: Operators

**Read first**: Operators section of the lesson.

**Part A** — Arithmetic. Predict each result before running:

```js
// console.log(10 + 3);  // Prediction:
// console.log(10 - 3);  // Prediction:
// console.log(10 * 3);  // Prediction:
// console.log(10 / 3);  // Prediction:
// console.log(10 % 3);  // Prediction: (What does % actually do?)
```

**Part B** — Comparison. Predict each, then explain the ones that surprise you:

```js
// console.log(5 === 5);    // Prediction:
// console.log(5 === "5");  // Prediction:
// console.log(5 !== 5);    // Prediction:
// console.log(5 > 3);      // Prediction:
```

**Part C** — Write a template literal that logs: `"10 plus 5 equals 15"`. Use variables for the numbers — do not hardcode the result.

**Part D** — Type coercion. Predict each result AND the resulting type:

```js
// console.log("5" + 5);     // Prediction:  Type:
// console.log("5" * 2);     // Prediction:  Type:
// console.log("5" - 2);     // Prediction:  Type:
// console.log(true + 1);    // Prediction:  Type:
// console.log("hello" * 2); // Prediction:  Type:
```

After running, answer as a comment: What pattern do you notice with `+` vs other operators when a string is involved?

**Commit when done**: `git commit -m "Complete operators and type coercion exercises"`

---

## Exercise 5: Conditional Logic

**Read first**: Conditional Logic section of the lesson.

**Part A** — Basic if/else. Change `isRaining` to `false`, predict what changes, then run to verify:

```js
const isRaining = true;

if (isRaining) {
  console.log("Don't forget your umbrella!");
} else {
  console.log("Enjoy the sunshine!");
}

// Prediction when isRaining = true:
// Prediction when isRaining = false:
```

**Part B** — Complete the grade checker. The `if` is done for you — fill in the missing `else if` conditions:

```js
const score = 85;

if (score >= 90) {
  console.log("A");
} else if (/* your condition */) {
  console.log("B");
} else if (/* your condition */) {
  console.log("C");
} else {
  console.log("F");
}
```

Test it by changing `score` to 95, 83, 72, and 60. Log what each produces as a comment.

**Part C** — Combining conditions. Predict whether each block logs its message, then uncomment to verify:

```js
const temp = 75;
const isSunny = true;

// if (temp > 70 && isSunny) {
//   console.log("Great day for a walk!"); // Logs?
// }

// if (temp > 90 || isSunny) {
//   console.log("At least one is true."); // Logs?
// }

// if (temp > 90 && isSunny) {
//   console.log("Both must be true."); // Logs?
// }
```

**Part D** — Write a time-of-day greeter. Given `hour` (0–23):

- 0–11 → `"Good morning!"`
- 12–17 → `"Good afternoon!"`
- 18–23 → `"Good evening!"`

Test with at least three different values of `hour`.

**Commit when done**: `git commit -m "Complete conditional logic exercises"`

---

## Other Commands

```bash
bun run lint    # Check for linting errors
bun run format  # Auto-format your code
```
