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
That’s what matters to me.

If something feels unfair, I’ll question it. If something breaks, I’ll say something. But I don’t want politics to become part of my identity. I don’t want to live my life in a permanent argument.

There are better things to do with my time.

That’s where I’m at right now. Maybe that’ll change. But for now, I’d rather focus on what I can actually control.

```dataview
TABLE WITHOUT ID
file.link AS "Entries",
file.day.year AS "Year"
FROM "7 - Journal/Daily"
WHERE dateformat(file.day, "MM-dd") = dateformat(this.file.day, "MM-dd")
AND file.day.year != date(today).year
SORT file.day ASC
```