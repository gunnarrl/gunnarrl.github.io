---
layout: essay
type: essay
title: "ESLint"
# All dates must be YYYY-MM-DD format!
date: 2025-02-12
published: true
labels:
  - ESLint
  - Coding Standards
---

<img width="200px" class="rounded float-start pe-4" src="../img/typescript.png">

# My Experience with ESLint and Coding Standards

## The Struggle with Coding Standards
Coding standards are important, but they can be a real pain to stick to—especially in timed environments like the WOD (a timed coding assessment). While they definitely help with consistency and readability, enforcing them while trying to code quickly can feel like an unnecessary burden. It’s frustrating when you’re racing against the clock and get slowed down by minor formatting issues. That being said, I do see the long-term benefits, and they do help reinforce good habits, even if they can be annoying in the moment.

## Frustrations with ESLint
Take ESLint, for example. My experience with it so far has been frustrating. Setting it up was a long and painful process, and I’m still not entirely sure everything is working correctly. One of my biggest issues is that it doesn’t display error messages in an inline comment; instead, you have to hover over the error to see what’s wrong. This slows down the debugging and cleanup process significantly. I also find some of the rules unnecessary. Does it really matter if my indentation is 2 spaces or 4? Sure, consistency is good, but when rules feel like they exist just for the sake of existing, it can be annoying.

### Example of Inconsistent Indentation
For example, ESLint may flag the following as an error due to inconsistent indentation:

```js
function example() {
    console.log("Hello, world!");
}
```

It might demand that the indentation be changed to:

```js
function example() {
  console.log("Hello, world!");
}
```

## Issues with AI-Generated Code
Another issue I’ve run into is ESLint’s interaction with AI-generated code. Tools like ChatGPT and Claude don’t produce code that adheres to ESLint’s standards, so if you use AI-generated snippets, you end up spending a ton of time just cleaning things up. This is especially frustrating when the AI-written code is functional but fails linting due to minor formatting issues. On the other hand, I guess this could be a good thing—it encourages me to write my own code instead of relying too much on AI.

### Example of AI-Generated Code
For instance, most LLMs might generate this:

```js
let num = 10;
if(num > 5) {
console.log("Greater than 5");
}
```

ESLint would likely flag it for improper indentation and use of whitespace, requiring a correction like this:

```js
let num = 10;
if (num > 5) {
  console.log("Greater than 5");
}
```

## Suggested Improvements for ESLint
A feature I mentioned earlier that would make ESLint much more useful and easier to use is inline comments for errors. Instead of requiring a mouse hover, an inline comment could instantly show what’s wrong:

```js
let x=5; // ESLint: Missing spaces around '='
console.log(x);
```

This would speed up the debugging process and make it easier to clean up code without constantly pausing to inspect errors. Instead, you would be able to see and solve the problem immediately.

## Positive Experience with VSCode
On the other hand, VSCode itself has been great. The integration with CoPilot makes coding faster and easier, though it did take some time to figure out how to properly run and view TypeScript code output through an HTML file. Installing all the necessary tools and extensions was tedious, but once everything was set up, the experience was smooth.

## Conclusion
Overall, I see the value in coding standards, but my experience with ESLint has been mixed. Some of its rules make sense and improve code quality, but others just feel like unnecessary hoops to jump through. When it comes to AI-generated code, ESLint can turn what should be a time-saving process into extra work. Still, I recognize that enforcing standards does have long-term benefits, even if it’s frustrating in the moment.

That being said, I’m hopeful that as I get more familiar with ESLint’s rules and configuration options, I’ll find a balance that maintains code quality without feeling overly restrictive. It might just take some time to get used to the workflow and figure out how to best integrate it into my coding process.

