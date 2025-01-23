---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Function Analysis"
date: 2024
published: true
labels:
  - Natural Language Processing
  - Data Science
  - Python
summary: "Analyzed the grammatical structure and use of abbreviations/acronyms in method names from Juypter notebooks for a paper at ICPC 2025"
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Most developers will spend well over 50% of their time looking at other peoples code. Because of this it is important that it adheres to standards for readability, in the field of software engineering this has been 
practiced for a long time, but new fields like data science lack these standards. So we manually evaluated around 500 jupyter notebooks looking for common grammar patterns in function names and when abbreviations 
or acrynoms are used. We found that the functions often had a similar grammar pattern, containing at least 1 noun and verb. But the main problem area was with the use of abbreviations and acrynoms. Functions would
commonly contain terms that were not defined in the surrounding code or markdown cells. This can lead to confusion with the functions purpose, and hinder other developers without domain knowledge.

We had a team of 4 people working on this paper, and work was shared equally. I worked on the manual review of the notebooks and the abbreviations/acrynoms analysis

The paper has been accepted for ICPC 2025 and will be available once it begins.
