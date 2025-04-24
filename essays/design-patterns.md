




# Navigating Complexity: Design Patterns in Manoa Compass

Software development often involves tackling recurring problems. **Design patterns** are reusable, well-tested blueprints for solving these common challenges, promoting code reusability, maintainability, and better team communication. Think of them as standard techniques for common building tasks, but for software.

Answering interview questions like "What are design patterns?" and "What design patterns have you used?" is easier with concrete examples. Here's how some patterns appeared in my Manoa Compass project for my software engineering class:

### Design Patterns Used in Manoa Compass

**1. Singleton (or Instance Management)**

* **Concept:** Ensures a class has only one instance and provides global access. Useful for managing shared resources like database connections.
* **Example (`src/lib/prisma.ts`):** We manage the Prisma client instance to avoid creating too many database connections, especially in development. The code checks for an existing global instance and reuses it, or creates a new one if needed.

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

* **Concept:** Allows objects with incompatible interfaces to work together by acting as a translator.
* **Example (`src/lib/authOptions.ts`):** The `PrismaAdapter` bridges the gap between NextAuth and our Prisma database, allowing NextAuth to manage users and sessions without needing specific Prisma knowledge.

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

* **Concept:** Defines a family of interchangeable algorithms, allowing the specific algorithm used to vary independently from the client code.
* **Example (`src/lib/authOptions.ts`):** NextAuth uses this for authentication providers. We defined `CredentialsProvider` as one strategy and could easily add others (like Google) later. We also selected the `jwt` session strategy.

    ```typescript
    // src/lib/authOptions.ts
    import CredentialsProvider from 'next-auth/providers/credentials';
    // import GoogleProvider from 'next-auth/providers/google';
    // ...

    export const authOptions: NextAuthOptions = {
      session: {
        strategy: 'jwt', // Choosing the JWT session strategy
      },
      providers: [ // Family of authentication strategies
        // GoogleProvider({ ... }),
        CredentialsProvider({ /* ... */ }), // Our chosen strategy
      ],
      // ...
    };
    ```

**4. Facade Pattern**

* **Concept:** Provides a simplified interface to a complex subsystem, hiding internal details.
* **Example (API Routes, e.g., `src/app/api/recommendations/route.ts`):** Our API routes act as facades. The `/api/recommendations` endpoint hides the complexity of fetching user interests, querying clubs and events, and applying logic, offering a simple interface to the frontend.

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

        // Return simplified result
        return NextResponse.json({ recommendedClubs, recommendedEvents });
      } catch (error) { /* ... */ }
    }
    ```

**5. Callback Pattern**

* **Concept:** Passing a function as an argument to another function, to be executed later.
* **Example (`src/lib/authOptions.ts`):** NextAuth uses callbacks (`jwt`, `session`, `signIn`) extensively, allowing us to customize its authentication flow, like adding user roles to the session token or verifying email domains.

    ```typescript
    // src/lib/authOptions.ts
    // ...
    export const authOptions: NextAuthOptions = {
      // ...
      callbacks: {
        async jwt({ token, user }) { /* Add data to token */ },
        async session({ session, token }) { /* Transfer token data to session */ },
        async signIn({ user, account, profile }) { /* Verify email domain */ }
      }
      // ...
    };
    ```

### Conclusion

Design patterns are practical tools for building robust and maintainable software. In Manoa Compass, patterns like Singleton, Adapter, Strategy, Facade, and Callbacks helped structure the application, integrate libraries, and manage complexity. Recognizing these patterns in my own code helps in discussing design choices effectively.
