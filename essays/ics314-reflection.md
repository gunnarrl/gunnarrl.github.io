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
# Reflections on Software Engineering: Beyond Building Web Pages

## I. Introduction

When I started Software Engineering I, I assumed the course would focus primarily on developing web applications. We followed a familiar web-development tech stack, HTML, CSS, JavaScript, React, Next.js and ultimately built [Manoa Compass](https://manoa-compass-code-theta.vercel.app/) as my final project. However, as we moved through the curriculum, I learned about software-engineering practices I had previously overlooked. I came to understand that techniques such as coding standards, Agile project management, and configuration management aren’t just “nice to have” for websites, they form the backbone of reliable, maintainable software in any domain.

## II. Insights on Coding Standards

At first, I thought coding standards were simply about keeping code neat. My main goal was to make my code run without crashing. Very quickly, though, I saw that coding standards are shared rules or guidelines that teams follow to write code in a uniform style—everything from how you name variables and functions to how you format braces and indentation.

For Manoa Compass, we adopted the Airbnb style guide via ESLint (configured in `.eslintrc.json`), plus Prettier rules in `.prettierrc.json`. ESLint pointed out naming inconsistencies (for example, whether to use `camelCase` versus `snake_case`), discouraged overly long functions, and enforced TypeScript type annotations. Prettier then formatted the code—line breaks, trailing commas, and quotation marks automatically. At first, fixing each lint error felt like chasing ghosts: I’d correct one issue and a new warning would pop up elsewhere. But over time, I appreciated how these tools eliminated bikeshedding arguments and shared code easier to understand and work with.

Beyond web apps, coding standards matter in any project where multiple people touch the same codebase, whether you’re using C, Python scripts for data analysis, or Java services for a back-end system. Uniform style reduces misunderstandings, prevents subtle bugs (like misnamed functions), and makes onboarding new collaborators much smoother. In my future work—whether a quick personal script or a large-scale team effort I want to strike a balance: enforce standards strictly on shared or production code, but defer the linter when sketching prototypes or proofs of concept.

## III. Applying Agile and Issue-Driven Project Management

Agile project management is a flexible methodology that breaks down work into small, incremental cycles (often called sprints), incorporates regular feedback, and adapts plans as needs evolve. A specific flavor we used is Issue-Driven Project Management (IDPM), where every piece of work like new features, bug fixes, and documentation updates are tracked as a GitHub issue. Branch names map directly to issue numbers (e.g., `issue-42`), so you always know exactly which task a given commit addresses.

Breaking the Manoa Compass roadmap into dozens of granular issues forced us to think carefully about scope. Writing clear issue descriptions (with acceptance criteria and screenshots) was harder than just coding the feature. Early on, our “Implement <page> backend” issues were too vague and we disagreed on what the requirments should be. After a few rounds of back-and-forth, we learned to create and follow a design document before writing any code.

Importantly, IDPM isn’t limited to web projects. I’ve already borrowed this practice for my research on automating code reviews with large-language models. By splitting the research pipeline into issues like data collection, baseline model evaluation, comment synthesis, and UI prototype. I could develop and test each piece in isolation, merge small PRs frequently, and revert if something broke unexpectedly. I could imagine using IDPM for laboratory experiments (each experiment or data-cleaning step as an issue), writing a book (chapters and edits as separate issues), or planning a community event (venue booking, promotion, volunteer coordination). The core idea is the same: track every discrete task, prioritize ruthlessly, and maintain clear documentation of what’s done and what’s next.

## IV. Embracing Configuration Management

Configuration management is the practice of systematically tracking and controlling all the settings, dependencies, and environments needed for your software to build and run reliably. In other words, it makes sure “it works on my machine” truly means “it works everywhere.”

During the Manoa Compass project, we hit several painful roadblocks: mismatched TypeScript compiler options, version drift between local and CI environments, and even a stale database migration that made a branch unusable. To fix this, we:

- Consolidated all dependencies in **`package.json`**, locking major versions to prevent accidental upgrades.  
- Synchronized compiler options in **`tsconfig.json`** so everyone’s VS Code and `npm run build` behaved identically.  
- Centralized end-to-end test settings in **`playwright.config.ts`**, ensuring the CI runner used the same viewport, timeouts, and credentials as local developers.  
- Automated continuous integration with **`.github/workflows/ci.yml`**, running lint checks, unit tests, and build scripts on every push.  
- Defined deployment behavior in **`vercel.json`** for smooth, repeatable rollouts.

While setting up configuration files and CI pipelines added overhead, it eliminated late-night “why did this deploy break?” emergencies. In larger teams—or any long-lived project—clear configuration management is indispensable. Even in small personal projects, I now see the value in at least version-locking dependencies and having a simple build script. It’s a discipline that pays dividends in reproducibility, onboarding speed, and overall project stability.

## V. Broader Impact on My Approach

The 3 practices of coding standards, issue-driven Agile, and configuration management have changed how I approach software work. I used to think programming was a solitary craft: write code, run it, ship it. Now, I see it as a collaborative, ongoing task between developers and tools. I write code not only for the computer to execute but for future team members (and my future self) to read, understand, and extend. I plan work not just to “get it done” but to deliver incremental value and maintain clear traceability. And I don’t trust makeshift environments; I record every step so that anyone can reproduce my results.

## VI. Challenges and Future Directions

Adopting these practices required overcoming a learning curve. Learning new languages, frameworks, linters, issue trackers, and configuration files can be overwhelming. It is tempting to prioritize getting code to work and postpone these processes. Yet I recognize that forming these habits early makes future collaboration and maintenance far easier. Although these tools may slow initial development, they provide long-term benefits by improving code quality and project organization.

## VII. Conclusion

In Software Engineering 1 I delivered far more than just a polished web application. It introduced me to the foundational practices that underpin professional software development: consistent coding standards, structured issue-driven workflows, and configuration management. These principles go beyond web applications and apply to any software or even non-software endeavor that requires collaboration, reliability, and clarity. As I continue my journey, I’m confident these lessons will guide me in crafting maintainable, high-quality solutions—no matter the platform or problem domain.
