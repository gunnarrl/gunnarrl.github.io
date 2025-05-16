---
layout: project
type: project
image: img/manoa-compass.png
title: "Manoa Compass"
date: 2025
published: true
labels:
  - AI
  - React
  - Web Development
summary: "Created an app that will have AI suggest events for you to attend on campus based on your profile."
---

# Project: Manoa Compass

## Overview

Manoa Compass is a dynamic web application designed to enhance student life at the University of Hawaii at Manoa (UHM) by connecting students with campus clubs and events. The platform aims to be a personalized guide, helping students discover opportunities aligned with their interests. Key features include a dashboard with event and club listings, user profile management with interest selection, and AI-powered recommendations to suggest relevant activities. The application also incorporates an administrative backend for content management, user oversight, and system operations, including automated web scraping to keep club and event information up-to-date.

As a developer on this project, I was instrumental in implementing several core functionalities. My primary contributions included the development of the **AI-powered suggestions** feature, leveraging Google's Generative AI to provide users with personalized event and club recommendations. I also engineered the **web scraping capabilities** for automatically gathering and categorizing club and event data from various sources, ensuring the platform's content remains fresh and comprehensive. Furthermore, I developed the **Admin page**, providing administrators with tools to manage content (events and clubs), users, categories, and oversee background jobs for data import and processing.

## What I Learned

This project was a valuable learning experience, allowing me to deepen my skills in full-stack development with Next.js and TypeScript. Implementing the AI suggestions provided insights into integrating and utilizing large language models for practical applications. Developing the web scraping and data categorization scripts (using tools like Cheerio and potentially Google Sheets API as suggested by `package.json` dependencies) honed my abilities in data extraction, processing, and automation. Building the admin dashboard reinforced my understanding of backend API development, database management with Prisma, user role management, and creating robust administrative interfaces. Working with NextAuth.js for authentication and managing various application states further enhanced my skills in building secure and interactive web applications.

## Screenshots

| **AI-Powered Suggestions / Dashboard**                       | **Profile Page**                                            |
| ------------------------------------------------------------- | ----------------------------------------------------------- |
| <img src="https://raw.githubusercontent.com/manoa-compass/manoa-compass.github.io/main/imgs/event_suggestion.png" alt="Dashboard" width="400px"> | <img src="https://raw.githubusercontent.com/manoa-compass/manoa-compass.github.io/main/imgs/profile_final.png" alt="Profile" width="400px"> |

| **Admin: Run Web Scraping**                                  | **Admin: Manage Events**                                    |
| ------------------------------------------------------------- | ----------------------------------------------------------- |
| <img src="https://raw.githubusercontent.com/manoa-compass/manoa-compass.github.io/main/imgs/admin_scraping.png" alt="Web Scraping" width="400px"> | <img src="https://raw.githubusercontent.com/manoa-compass/manoa-compass.github.io/main/imgs/admin_manage_events.png" alt="Manage Events" width="400px"> |


  
## Source Code & More

For those interested in diving deeper into the technical aspects or viewing the source code, please visit the project's GitHub Organization page:

[Link to Manoa Compass GitHub Organization](https://github.com/manoa-compass)
