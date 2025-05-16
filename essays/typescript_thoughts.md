---
layout: essay
type: essay
title: "The Good and Bad of TypeScript"
# All dates must be YYYY-MM-DD format!
date: 2025-01-22
published: false
labels:
  - Typescript
---

<img width="200px" class="rounded float-start pe-4" src="../img/typescript.png">

## Thoughts on TypeScript
TypeScript is an interesting language, but I have mixed feelings about it. Coming from a Python background, I’m used to the flexibility of dynamically-typed languages, and TypeScript’s static typing feels a bit restrictive. That said, I understand how it’s helpful for catching type errors early. For example:

```typescript
function calculateTotal(price: number, quantity: number): number {
  return price * quantity;
}
calculateTotal("10", 5); // Error: Argument of type 'string' is not assignable to 'number'
```

This saved me from runtime bugs, especially in complex projects where those errors can be harder to track down.

## What I Like About TypeScript
One thing I do appreciate about TypeScript is how it builds on JavaScript. If you know JavaScript, it’s not too hard to pick up. You still get to use what you already know, but with added features like interfaces and type annotations. This makes it easier to write code that’s more reliable and maintainable, both of which are important for software engineering. Using what I know from JavaScript, it’s easy to adopt features like interfaces:

```typescript
interface Product {
  id: string;
  name: string;
  price: number;
}

function displayProduct(product: Product) {
  console.log(`${product.name}: $${product.price}`);
}
```

This makes codebases more maintainable, a big plus for team projects.

## What I Don’t Like
What I don’t like as much is how structured it is. I’m used to quickly experimenting in Python without worrying about types, so having to define everything upfront in TypeScript can feel like extra work, especially for small projects or prototypes. It’s a trade-off where you give up some speed and flexibility for more safety and clarity in the long run. In Python, I’d write:

```python
# Python: Just use a dictionary!
product = {"id": "123", "name": "Coffee", "price": 4.99}
```

But in TypeScript, I have to define types even for quick tests:

```typescript
type Product = { id: string; name: string; price: number };
const product: Product = { id: "123", name: "Coffee", price: 4.99 };
```

## Final Thoughts 
Overall, while I don’t love TypeScript personally, I can see why it’s popular. Catching bugs before runtime make it solid for teams and complex codebases. For me, it’s about using the right tool for the job, TypeScript for structure and Python/Javascript for speed.



