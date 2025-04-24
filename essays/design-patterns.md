---
layout: essay
type: essay
title: "Recipe to Success: Design Patterns"
# All dates must be YYYY-MM-DD format!
date: 2025-04-24
published: true
labels:
  - Software Development
  - Manoa Compass
---
<img style="width: 400px !important;" class="rounded float-start pe-5" src="https://img.freepik.com/free-vector/recipe-book-kitchenware_1284-35619.jpg?semt=ais_hybrid&w=740">


# Navigating Complexity: Design Patterns in Manoa Compass

Software development often involves tackling recurring problems. **Design patterns** are reusable, well-tested blueprints for solving these common challenges, promoting code reusability, maintainability, and better team communication. Think of them as a recipe for common building tasks but for software; this way, you don't have to start from scratch every time you open or join a new project. Instead, you can look at your "recipe book" (design patterns) and have an easy way to get started or up to speed.

Answering interview questions like "What are design patterns?" and "What design patterns have you used?" is easier with concrete examples. Here's how some patterns appeared in my Manoa Compass project for my software engineering class. Some of these were already existing from the Next.js template we used, but they still serve as good examples of these recipes in action:

### Design Patterns Used in Manoa Compass

**1. Singleton (or Instance Management)**

* **Concept:** Ensures a class has only one instance and provides global access. Useful for managing shared resources like database connections. (Think of having only one master spice jar for a rare ingredient).
* **Example (`src/lib/prisma.ts`):** We manage the Prisma client instance to avoid creating too many database connections, especially in development. The code checks for an existing global instance and reuses it, or creates a new one if needed. This pattern was adapted from common Next.js practices for database clients.

    ```typescript
    // src/lib/prisma.ts
    import { PrismaClient } from '@prisma/client';

    const globalForPrisma = global as unknown as { prisma: PrismaClient };

    export const prisma =
      globalForPrisma.prisma ||
      new PrismaClient({ log: ['query'] });

    if (process.env.NODE_ENV !== 'production') globalForPrisma.prisma = prisma;
    ```

**2. Adapter Pattern**

* **Concept:** Allows objects with incompatible interfaces to work together by acting as a translator. (Like using a measuring cup adapter for metric vs. imperial units in a recipe).
* **Example (`src/lib/authOptions.ts`):** The `PrismaAdapter` (provided by NextAuth) bridges the gap between NextAuth's requirements and our Prisma database schema, allowing NextAuth to manage users and sessions without needing specific Prisma knowledge.

    ```typescript
    // src/lib/authOptions.ts
    import { PrismaAdapter } from '@next-auth/prisma-adapter';
    import { prisma } from '@/lib/prisma';
    // ...

    export const authOptions: NextAuthOptions = {
      adapter: PrismaAdapter(prisma), // Adapter connects NextAuth to Prisma
      // ...
    };
    ```

**3. Strategy Pattern**

* **Concept:** Defines a family of interchangeable algorithms, allowing the specific algorithm used to vary independently from the client code. (Like having different recipes for cooking potatoes – baking, boiling, frying – that you can choose from).
* **Example (`src/lib/authOptions.ts`):** NextAuth uses this for authentication providers (part of the library's design). We configured the `CredentialsProvider` as one strategy (recipe) for logging in. We could easily add others (like `GoogleProvider`) later without rewriting the core login flow. We also selected the `jwt` session strategy.

    ```typescript
    // src/lib/authOptions.ts
    import CredentialsProvider from 'next-auth/providers/credentials';
    // import GoogleProvider from 'next-auth/providers/google';
    // ...

    export const authOptions: NextAuthOptions = {
      session: {
        strategy: 'jwt', // Choosing the JWT session strategy
      },
      providers: [ // Family of authentication strategies (recipes)
        // GoogleProvider({ ... }),
        CredentialsProvider({ /* ... */ }), // Our chosen strategy
      ],
      // ...
    };
    ```

**4. Facade Pattern**

* **Concept:** Provides a simplified interface to a complex subsystem, hiding internal details. (Like a pre-made sauce mix that simplifies making a complex dish).
* **Example (API Routes, e.g., `src/app/api/recommendations/route.ts`):** Our API routes act as facades (part of the Next.js API structure). The `/api/recommendations` endpoint hides the multiple steps involved (fetching user data, querying clubs/events, filtering) and offers a simple interface to the frontend.

    ```typescript
    // src/app/api/recommendations/route.ts
    // ... imports
    export async function GET(/* ... */) {
      // ... authorization check ...
      try {
        // Complex steps hidden from the caller:
        // 1. Get user interests
        // 2. Query clubs
        // 3. Query events
        // 4. Apply fallback logic (if needed)

        // Return simplified result (the finished dish)
        return NextResponse.json({ recommendedClubs, recommendedEvents });
      } catch (error) { /* ... */ }
    }
    ```

**5. Callback Pattern**

* **Concept:** Passing a function as an argument to another function, to be executed later. (Like a recipe step saying "mix until combined, *then* add eggs").
* **Example (`src/lib/authOptions.ts`):** NextAuth relies heavily on callbacks (part of its design) like `jwt`, `session`, and `signIn`. These allow us to inject custom steps into its authentication process, like adding user roles to the session token *after* the token is created, or verifying email domains *before* sign-in completes.

    ```typescript
    // src/lib/authOptions.ts
    // ...
    export const authOptions: NextAuthOptions = {
      // ...
      callbacks: { // Points where we inject custom steps into the NextAuth recipe
        async jwt({ token, user }) { /* Add data to token */ },
        async session({ session, token }) { /* Transfer token data to session */ },
        async signIn({ user, account, profile }) { /* Verify email domain */ }
      }
      // ...
    };
    ```

### Conclusion

Design patterns are like well-tested recipes in our software development cookbook. They provide practical, reusable solutions that help build robust and maintainable applications. In Manoa Compass, patterns like Singleton, Adapter, Strategy, Facade, and Callbacks – some implemented by us, others leveraged from the Next.js template and libraries like NextAuth – were essential. They helped structure the application, integrate different parts smoothly, and manage complexity. Recognizing these patterns, whether we wrote them from scratch or used them from a framework, is key to understanding the codebase and discussing design choices effectively. Having this "recipe book" allows developers to avoid starting from scratch and quickly get up to speed on building common software features.

