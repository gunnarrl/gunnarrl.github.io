---
layout: essay  
type: essay  
title: "Reflections on Software Engineering: Beyond Building Web Pages"  
# All dates must be YYYY-MM-DD format!  
date: 2025-05-14
published: true
labels:  
 - Software Engineering  
---

# Reflections on Software Engineering: Beyond Building Web Pages

## I. Introduction

When I started **Software Engineering I**, I assumed the course would focus primarily on developing web applications. We followed a web-development tech stack and created **Manoa Compass** as our final project. However, as we progressed, I gained firsthand experience with fundamental software-engineering concepts that I had previously overlooked. I realized that practices such as **coding standards**, **Agile project management**, and **configuration management** are valuable across all types of software development, not just web applications.

## II. Insights on Coding Standards

Initially, I thought coding standards were simply about keeping code tidy. My priority was making my code run correctly. Early in the course, I discovered that coding standards are crucial for teamwork and maintaining code quality over time. These standards are shared rules for writing code consistently.

For **Manoa Compass**, we used ESLint with an `​.eslintrc.json` configured for the Airbnb style guide, along with rules for Next.js and TypeScript. ESLint flagged naming issues and structural inconsistencies, while a `.prettierrc.json` file handled automatic formatting. Having a uniform style made reading and modifying teammates’ code much easier. Admittedly, dealing with ESLint warnings could be frustrating—fixing one issue sometimes introduced another. Despite this, I now appreciate its value and plan to use ESLint for collaborative or large-scale projects. For small personal projects, however, I may focus on functionality first and the linter later.

## III. Applying Agile and Issue-Driven Project Management

“Agile project management” was another term I had heard but never fully understood. I now see it as an approach that breaks work into small, flexible increments and adapts as needs change. In class, we adopted **Issue-Driven Project Management (IDPM)**, which uses GitHub issues for tasks, bugs, and feature requests. We named our branches `issue-XXX` to match each task.

Breaking large features into well-defined issues was challenging—sometimes our issues lacked clear goals or specifications, leading to confusion. I learned the importance of writing precise, agreed-upon issue descriptions. This semester, I applied IDPM to my research on automating code reviews with large language models. Dividing the project into granular issues made it easier to develop and test each component. IDPM is not limited to web development; it could structure laboratory experiments or any complex endeavor.

## IV. Embracing Configuration Management

Configuration management might sound mundane, but it proved essential. It involves tracking the settings, tools, and versions needed to ensure software runs consistently everywhere.

Early in the Manoa Compass project, inconsistencies in database schemas and library versions caused our code to break. We resolved this by:

- Consolidating dependencies in `package.json`
- Synchronizing TypeScript settings in `tsconfig.json`
- Standardizing test configuration in `playwright.config.ts`
- Automating builds with `.github/workflows/ci.yml`
- Configuring deployment with `vercel.json`

Although setting up and maintaining these files can be time-consuming, the payoff is a stable, reproducible development environment. For large teams or long-term projects, configuration management is indispensable; for smaller personal efforts, it can feel like overkill but remains a helpful discipline.

## V. Broader Impact on My Approach

Using coding standards, issue-driven project management, and configuration management completely changed how I think about software development. I used to treat coding as just giving instructions to a computer. Now, I see it more as writing for other people—making sure my code is readable, flexible, and dependable no matter where it’s run. Even though Manoa Compass was a web project, these lessons apply to any serious software project.

## VI. Challenges and Future Directions

Adopting these practices required overcoming a learning curve. Learning new languages, frameworks, linters, issue trackers, and configuration files can be overwhelming. It is tempting to prioritize getting code to work and postpone these processes. Yet I recognize that forming these habits early makes future collaboration and maintenance far easier. Although these tools may slow initial development, they provide long-term benefits by improving code quality and project organization.

## VII. Conclusion

**Software Engineering I** offered much more than the creation of Manoa Compass. The key lessons I will carry forward are the significance of coding standards, the structure of issue-driven work management, and the necessity of configuration management. These skills extend well beyond web projects and form the foundation of professional software engineering. I am confident that they will guide me in any development effort I undertake in the future.
