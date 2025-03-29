---
layout: post
title: Forever Notes in Obsidian
date: 2025-03-29
tags:
  - Productivity
tags_color: "#de47e2"
image: https://media.anantshiva.com/obsidian-forever-notes.jpg
description: 
video_embed: https://www.youtube.com/embed/DqKfBQNn_vE?si=zvJkyNNX-vWfWbQ_
featured:
---
When I first stumbled upon the _Forever Notes_ journal setup in Apple Notes, it felt like a cheat code for self-awareness. Imagine opening today’s entry and instantly looking at what you were thinking, feeling, or struggling with on this exact day, last year, and the year before that. 

It’s like time-travel therapy. Honestly, I'm not sure why every journaling app didn’t already work this way. Once you see it, you can’t unsee it.

In the meantime, Forever Notes works. Though it's a hassle to set up. 

I know because I painstakingly migrates my journal entries one by one to Apple Notes and journalled this way for a couple of months. In the process, I came across entries that I'd completely forgotten about. 

```js
TABLE WITHOUT ID
file.link AS "Entries",
file.day.year AS "Year"
FROM "7 - Journal/Daily"
WHERE dateformat(file.day, "MM-dd") = dateformat(this.file.day, "MM-dd")
AND file.day.year != date(today).year
SORT file.day ASC
```