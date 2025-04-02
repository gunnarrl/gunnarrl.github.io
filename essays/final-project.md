---
layout: essay  
type: essay  
title: "Manoa Compass Proposal"  
# All dates must be YYYY-MM-DD format!  
date: 2025-04-01  
published: true
labels:  
 - Software Engineering  
 - Nextjs  
---

## Overview

**The Problem:** 
31% of students at UH Manoa are out of state with 8% being international. For many of these students, it is their first time in Hawaii and they have no idea what there is to do around campus and in the state itself. Simply searching for things on Google Maps can take time, and often leads to minimal activities to do. Unfortunately, this leads to students having a lack of things to do and leads to increased stress and feelings of isolation.

**The Solution:**  
**Manoa Compass** is a web application that students attending UH Manoa can log in to with their school email and make a profile that has their interests, major, where they're from, and housing and transportation situation. Using AI, we will create a To-Do list for this incoming student to get the full experience of Hawaii catered to their profile. This will allow for the student to discover their favorite spots on the island and activities to do while they are going to school here.


## Mockup Page Ideas

- **Landing Page:**  
  - Welcomes new visitors and prompts them to log in or sign up with their UH Manoa email.
  
- **User Profile Page:**  
  - Allows users to input their interests, major, hometown, housing details, and transportation options.
  
- **To-Do List Page:**  
  - Displays a dynamic, AI-generated list of recommended activities and locations.
  
- *(Optional)* **Explore/Map Page:**  
  - Interactive map showcasing recommended spots, with filters based on categories (e.g., food, outdoor, cultural).

## Use Case Ideas

The initial implementation will be minimal, but here’s an overview of an end-to-end scenario:

1. **New User Registration:**  
   - *Step 1:* User lands on the **Landing Page** and is prompted to log in using their UH Manoa email.
   - *Step 2:* Upon logging in, the user is taken to the **User Profile Page**, where they enter personal details (interests, major, hometown, etc.).
   - *Step 3:* The system confirms the profile setup and explains that an AI-driven process will soon generate a personalized to-do list.

2. **Receiving Personalized Recommendations:**  
   - *Step 4:* Once the profile is complete, the user is redirected to the **To-Do List Page**, where they see a curated list of activities and destinations around campus and across the island.
   - *Step 5:* The user can click on each recommendation to view more details, such as location, suggested time to visit, and any special notes on the activity.

3. **Interaction and Feedback:**  
   - *Step 6:* After visiting a location or trying an activity, the user can leave feedback or rate the experience.
   - *Step 7:* This feedback is then used to refine future recommendations for the user and others with similar interests.

## Beyond the Basics

Once the core functionality is in place, additional features could enhance the user experience:

- **Advanced Notification System:**  
  - *Real-Time Alerts:* Send notifications (via email, SMS, or in-app) when new recommendations or nearby events align with the user’s profile.
  - *Calendar Integration:* Allow users to add recommended events or activities directly to their digital calendars (e.g., Google Calendar).

- **Social and Community Features:**  
  - *Sharing and Collaboration:* Enable users to share their to-do lists or favorite spots with friends and classmates.
  - *Community Reviews:* Incorporate a system where users can post reviews or comments on the recommended activities, providing additional insights to peers.

- **Enhanced Personalization:**  
  - *Dynamic Updates:* Continuously update recommendations based on user behavior (e.g., what they click on or rate highly).
  - *Interactive Map Integration:* Provide an interactive map view where users can see locations and get directions, along with contextual information about each spot.

- **Administrative and Analytics Tools:**  
  - *User Analytics:* Allow administrators to monitor user engagement and identify trends in activity preferences.
  - *Content Management:* Enable admins to update and curate certain activities or special campus events to ensure the recommendations remain relevant and timely.

By combining AI-driven personalization with community feedback and robust integration features, **Manoa Compass** aims to transform the way students explore their new home, making campus life richer and more connected from day one.
