---
layout: essay  
type: essay  
title: "Reflections on AI in Software Engineering"  
# All dates must be YYYY-MM-DD format!  
date: 2025-05-06
published: true
labels:  
 - Software Engineering  
 - AI
---

# Reflections on AI in Software Engineering: My Experience in ICS 314

## I. Introduction

Artificial intelligence is becoming a bigger part of education, and that's definitely true for Software Engineering. I think that using AI can be really helpful for learning, and I use it quite a bit in all my classes. The trick is knowing how to use it the right way, so you're still learning things yourself and not just letting the AI do all the work. For coding specifically, I found AI tools like ChatGPT, Claude, Gemini, and GitHub Copilot pretty great. I mostly used the latest free versions available during the semester. My main approach, especially in ICS 314, was to use AI for writing basic code outlines or handling the tedious parts I didn't want to write from scratch. Then, I could focus on refining the code and tweaking the small things to get it working correctly. I used these tools most often to help me complete Workouts of the Day (WODs) or figure things out when I got stuck on practice WODs.

## II. Personal Experience with AI

My use of AI varied depending on the specific part of the ICS 314 course. Here's a breakdown:

* **Experience WODs (e.g., E18):** I definitely used AI on these whenever I got stuck. For example, during the digits E-WOD series, my process was usually to try it on my own first. If I couldn't figure out what was wrong after about five minutes, I'd turn to AI. I specifically remember getting stuck on implementing the edit contacts feature in part 5. I gave the AI (likely ChatGPT or Claude) my problematic files, explained I wanted to allow users to edit contacts, and asked what was wrong with my code. Since these WODs weren't timed, AI was super helpful. You could almost always get an answer eventually, though the more complex the problem, the more careful you had to be with your prompt to get what you needed. It saved a lot of time compared to Googling, and often the initial answer worked perfectly.
* **In-class Practice WODs:** I generally tried *not* to use AI for these. Since they weren't graded and were meant for practicing new concepts, I felt it was more important to struggle through them myself. I saw them as pure practice, so it didn't matter if I didn't finish or get it perfect. I only considered AI if I was completely lost.
* **In-class WODs:** Here, I used AI almost every time. The time limit made AI a huge help, and the WODs would have been much harder without it. My strategy was to understand the basic requirements, have AI generate the initial code, and then I'd refine the specifics. However, it wasn't always helpful. I remember one HTML WOD where the AI kept insisting I use import/export statements. That wasn't right for how we were supposed to set up the `index.html` file. It took showing the AI the error message about 20 times before it understood. So, sometimes it cost more time than it saved.
* **Essays:** For essays, like this reflection, my AI use was limited. I mainly used it to help check my Markdown formatting or to get suggestions for improving sections I had already written myself. I'd paste my text and ask something like "Can you suggest ways to make this paragraph clearer?"
* **Final project:** Honestly, I pretty much "vibe coded" my parts of the final project. AI wrote almost every line of code for my contribution. I was able to use a free trial of Gemini 2.5 Pro for this, which let me attach my whole code folder. This made a massive difference because the AI had context for the entire project and understood my requests much better. It saved me potentially hours and hours of struggle. Trying to figure out all that code myself would have been really tough. It managed to complete all the tasks I asked, though some things, like writing webscraping scripts, required more back-and-forth.
* **Learning a concept / tutorial:** Yes, I used AI quite a bit here. When I was first learning PostgreSQL, I asked AI tons of questions about setting it up correctly and understanding the commands. Things like `npx prisma migrate`, `deploy`, `generate`, etc., kept breaking when I tried them on my own. AI helped me actually understand what each command did and how to use it properly.
* **Answering a question in class or in Discord:** I didn't use AI for this. It just felt kind of weird to type someone's question into an AI and then just paste the answer back. It didn't feel like my own thoughts or contribution, even though technically it's similar to using it for an assignment. The social aspect made me avoid it here.
* **Asking or answering a smart-question:** I didn't directly use AI to formulate a smart question or answer one. However, I did answer a few questions in Discord using knowledge I'd gained from interacting with AI while working on an assignment earlier. I don't recall the specific question, though. This wasn't a major use case for me.
* **Coding example (e.g., “give an example of using Underscore .pluck”):** I don't think I ever asked AI for just a simple coding example in this class. Because there were so many assignments, I was always asking it to write code *for* one of those assignments, not just for a generic example. I do use it for examples frequently in my algorithms class, though.
* **Explaining code:** Yes, I did this often, especially asking the AI to explain the code *it* had just generated for me. This helped me understand how it worked and what parts I needed to change. For instance, when working on the webscraping scripts for the final project, which was new to me, I asked the AI to break down each part of its script. This allowed me to modify it correctly to gather the specific data we needed.
* **Writing code:** As mentioned, AI did a lot of the heavy lifting here. It wrote significant portions of code for E-WODs, in-class WODs, and especially the final project.
* **Documenting code:** The main way I used AI for documentation was getting help writing pull requests. After I finished working on a branch, I'd ask AI to help draft the pull request description. It was good at writing it like an experienced programmer would, including sections I might have forgotten.
* **Quality assurance (e.g., “What’s wrong with this code <code here>” or “Fix the ESLint errors in <code here>”):** I specifically used GitHub Copilot for fixing ESLint errors. Its integration into VSCode was super convenient, meaning I didn't have to switch tabs. The code generated by other AIs often had many ESLint issues related to typing, nested ternaries, missing properties, and so on. Copilot was great at fixing these, usually getting it right on the first try.
* **Other uses in ICS 314 not listed:** I can't think of any other major ways I used AI specifically for this course.

## III. Impact on Learning and Understanding

Reflecting on it, I think I probably would have learned more, or at least learned more deeply, if I hadn't used AI so much in ICS 314. There's value in "getting reps in" when you're learning to code, and also in learning how to solve problems yourself without immediately copy-pasting into ChatGPT. Without AI, I likely would have spent much more time grappling with the concepts and might have built a stronger foundation. But, I used the tools available to me. AI definitely made implementing concepts easier and faster. However, I feel it hurt my core problem-solving skills. My first instinct when facing a coding challenge or bug now is often just to ask AI, rather than trying to debug it myself first.

## IV. Practical Applications

I've used AI quite a lot for software engineering tasks outside of ICS 314 too. I've been involved in research with Dr. Peruma for the past two years, and I regularly use AI to help write code for research tasks. For example, this semester I used it to help develop code that performs AI-based code reviews on a collection of Jupyter notebooks. I also used AI extensively during my summer internship to help with tasks involving the R language, specifically for analyzing and visualizing data we collected. In all these different contexts, I've found AI to be very helpful and effective.

## V. Challenges and Opportunities

For me, the biggest challenge in using AI effectively is writing good prompts. Getting the AI to understand exactly what you need, especially for complex tasks, takes practice. Beyond that, I think the risk of over reliance is huge. It seems almost inevitable that people will become dependent on it; that just feels like the direction things are going. In terms of education, I think it's important to teach students *how* to ask AI good questions, maybe using methods like the SMART criteria we learned. But, I also strongly believe there need to be assignments or parts of courses where AI use is explicitly forbidden, so students are forced to develop their own skills.

## VI. Comparative Analysis

Comparing my AI enhanced learning in ICS 314 to traditional methods, there's a clear trade off. Without AI, I think I would have learned the topics we covered much more deeply. With AI, I was able to cover more ground, learn about more concepts, and complete more complex tasks than I likely could have otherwise. So, it's breadth versus depth. Personally, I find screencasts to be the best way to learn, but using AI is definitely better for me than just reading a textbook, which never really worked well for me. AI can explain complex topics in a simpler, less formal way that's easier to understand. However, for actual skill development, particularly coding skills, I think relying heavily on AI actively makes you worse. If you compare me to someone who took this class, say, eight years ago before these AI tools were common, their fundamental coding ability and problem solving skills would likely be much better developed.

## VII. Future Considerations

Looking ahead, I think AI absolutely has to be part of software engineering education because it's clearly the future of the field. Developers are going to be using these tools constantly. But it needs to be integrated thoughtfully. I still believe it's critical for students to sometimes write code entirely on their own. Finding the right balance and figuring out how to enforce non AI work is the challenge. I am quite worried that advanced AI might start taking over the jobs typically done by junior developers, since AI is getting very good at writing standard code for common tasks. This might mean that software engineering education needs to shift its focus, perhaps emphasizing skills like system design, complex problem solving, prompt engineering, or AI oversight, rather than just basic coding implementation.

## VIII. Conclusion

Overall, my experience in ICS 314 showed me that AI is an incredibly powerful and useful tool for software engineering students. It can save time, help overcome roadblocks, and even assist in understanding complex topics. However, it's also a tool that makes over reliance extremely easy, potentially hindering the development of fundamental coding and problem solving skills. Honestly, it feels a bit like a drug sometimes; once you see how well it can do one task, you want it to do the next one, and then the next, until your first reaction to any problem is just to ask the AI. My main recommendation for optimizing AI integration in future courses would be to ensure there's at least a small, clearly defined part of the course perhaps specific assignments or exams where AI use is strictly prohibited. This would force students to build and demonstrate those foundational skills that are still crucial, even in an AI driven world.

