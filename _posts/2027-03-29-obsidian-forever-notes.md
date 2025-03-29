---
layout: post
title: How to Time Travel in Obsidian - Inspired by Forever Notes
date: 2025-03-29
tags:
  - Productivity
tags_color: "#de47e2"
image: https://media.anantshiva.com/obsidian-forever-notes.jpg
description: 
video_embed: https://www.youtube.com/embed/DqKfBQNn_vE?si=zvJkyNNX-vWfWbQ_
featured:
---
When I first stumbled upon the [Forever Notes](https://www.myforevernotes.com) journal setup in Apple Notes, it felt like a cheat code for self-awareness. Imagine opening today’s entry and instantly looking at what you were thinking, feeling, or struggling with on this exact day, last year, and the year before that. 

It’s like time-travel therapy. Honestly, I'm not sure why every journaling app didn’t already work this way. Once you see it, you can’t unsee it.

In the meantime, Forever Notes works. Though it's a pain in the ass to set up. 

I know because I manually migrated my journal entries one by one to Apple Notes and journaled this way for a couple of months. In the process, I came across entries that I'd completely forgotten about. I laughed, I cried - ok, I didn't *cry*. But I did get emotional. It was surprisingly cathartic.

I was loving it.

Until I realised that I could do the same thing in Obsidian with a single Dataview query. Here’s what I use in the Daily Notes template to pull past entries from the same date:

```css
TABLE WITHOUT ID
file.link AS "Entries",
file.day.year AS "Year"
FROM "7 - Journal/Daily"
WHERE dateformat(file.day, "MM-dd") = dateformat(this.file.day, "MM-dd")
AND file.day.year != date(today).year
SORT file.day ASC
```

"7 - Journal/Daily" is where my journal entries live. You’ll want to change that to wherever you keep your journal entries. You obviously need the Dataview plugin for this to work. 

I’ve now moved my journaling back to Obsidian - and I use it for long-form writing, note-taking, and this blog as well. But do I still miss Apple Notes?  Yes. I have a problem.