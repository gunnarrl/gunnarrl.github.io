---
layout: essay  
type: essay  
title: "Reflections on Software Engineering"  
# All dates must be YYYY-MM-DD format!  
date: 2025-05-14
published: true
labels:  
 - Software Engineering  
---
# Software Engineering: Beyond Building Web Pages

## I. Introduction

Upon commencing Software Engineering I, my initial assumption was that the course would primarily focus on the development of web applications, a perception reinforced by the utilization of a web-development technology stack and the creation of Manoa Compass as our final project. However, as the semester progressed and our team engaged more deeply with this project, a firsthand appreciation for fundamental software-engineering concepts, previously less considered, began to form. It became evident that practices such as coding standards, Agile project management, and configuration management possess a utility that extends far beyond web applications, proving valuable across the diverse spectrum of software development.

## II. Insights on Coding Standards

Initially, coding standards were perceived as guidelines primarily concerned with aesthetic code presentation, with the overriding priority being functional correctness. Early in the course, however, it became clear that coding standards are crucial for effective teamwork and the long-term maintainability of code quality. These standards represent a shared set of conventions for writing code consistently.

For the Manoa Compass project, this was put into practice through tools like ESLint, configured via an `.eslintrc.json` file for the Airbnb style guide with additional rules for Next.js and TypeScript. This ESLint setup identified deviations in naming conventions and code structure, while a `.prettierrc.json` file managed automatic code formatting. The establishment of a uniform style greatly facilitated the comprehension and modification of code authored by different team members. Admittedly, adherence to ESLint warnings occasionally proved frustrating, as resolving one flagged issue could sometimes inadvertently introduce others. Despite this, the value of such tools is now well appreciated, and their use is anticipated for future collaborative or large-scale projects. For smaller, personal endeavors, however, a primary focus on functionality might precede rigorous linter compliance.

## III. Applying Agile and Issue-Driven Project Management

“Agile project management” was another term encountered prior to this course, though its practical implications were not fully understood. It is now recognized as an approach that structures work into small, flexible increments, adapting to changes as they arise, rather than rigidly adhering to a predefined long-term plan. In class, an effort was made to adopt Issue-Driven Project Management (IDPM), a specific Agile methodology that utilizes GitHub issues to delineate tasks, bugs, and feature requests. Correspondingly, Git branches were named using an `issue-XXX` convention to clearly link development work to specific tasks.

The decomposition of large features into well-defined, granular issues presented a notable challenge; at times, our issues lacked precise goals or detailed specifications, which occasionally led to ambiguity during implementation. For example, tasks described simply as "implement event backend" offered insufficient guidance. This experience underscored the importance of formulating precise, agreed-upon issue descriptions. On a positive note, the IDPM approach has proven effective in my current research on automating code reviews with large language models; dividing this complex project into smaller, distinct issues has significantly streamlined the development and testing of individual components. The principles of IDPM are clearly not limited to web development and could be beneficially applied to structure diverse complex endeavors, such as laboratory experiments or extensive research papers.

## IV. Embracing Configuration Management

Configuration management, while perhaps a less salient topic, proved to be an essential discipline. It involves the systematic tracking and control of settings, tools, and component versions necessary to ensure that software operates consistently across various environments.

Early in the Manoa Compass project, inconsistencies in individual database schemas and library versions among team members led to integration challenges and necessitated code revisions. These issues were largely resolved by implementing more rigorous configuration management practices, including:

-   Consolidating project dependencies and their specific versions within the \`package.json\` file.

-   Synchronizing TypeScript compiler settings through a shared `tsconfig.json`.

-   Standardizing the testing environment configuration using `playwright.config.ts`.

-   Automating build and test processes via a `.github/workflows/ci.yml` file.

-   Defining environment-specific settings, such as local development data in `config/settings.development.json`.

-   Configuring deployment parameters and scheduled tasks, like cron jobs for data scraping, using `vercel.json`.

Although the initial setup and ongoing maintenance of these configuration files can be time-consuming, the resulting stability and reproducibility of the development environment are significant. For large teams or long-term projects, meticulous configuration management is indispensable. For smaller personal efforts, while the full extent of these practices might seem substantial, the underlying discipline remains beneficial.

## V. Broader Impact on My Approach

The application of coding standards, issue-driven project management, and configuration management has fundamentally reshaped my perspective on software development. Previously, the act of coding was viewed primarily as instructing a computer to perform tasks. It is now understood more as a form of communication, emphasizing readability for other developers, adaptability to change, and operational consistency across diverse environments. Although Manoa Compass was a web-based project, these engineering principles are pertinent to any serious software undertaking.

## VI. Challenges and Future Directions

Adopting these software engineering practices necessitated overcoming an initial learning curve. When simultaneously acquiring new programming languages and frameworks, the additional layers of linters, issue trackers, and configuration files can appear overwhelming. It is often tempting to prioritize immediate functionality and defer adherence to these structured processes. Yet, it is increasingly evident that cultivating these habits early in one's development journey significantly facilitates future collaboration and long-term project maintainability. While these tools and methodologies may occasionally seem to slow initial development, their long-term contributions to code quality and project organization are substantial.

## VII. Conclusion

Software Engineering I offered considerably more than the technical skills required for the creation of the Manoa Compass application. The enduring lessons from this course are centered on the significance of robust coding standards, the structured approach of issue-driven work management, and the critical necessity of thorough configuration management. These competencies extend well beyond the domain of web projects and form a crucial part of the foundation for professional software engineering. It is anticipated that these principles will provide valuable guidance in any future development efforts undertaken.
