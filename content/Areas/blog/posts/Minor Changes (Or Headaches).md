---
title: Minor Changes (Or Headaches)
creation date: 2024-10-07
modified:
  - 2024-10-03T23:15:49-07:00
  - 2024-10-07T15:59:58-07:00
  - 2024-10-07T16:09:20-07:00
---
Tending to the garden that I've been neglecting for the summer. 

The main change I wanted to make, is adding a recent notes section. 
The act of adding a [[Recent Notes]](that's not just a page that I manually maintain) section was easy.

It was as simple as going into my [[Quartz]] directory and adding the Recent Notes component to quartz.layout.ts

The issue that has been plaguing me for the past couple weeks is that every time I sync my garden, with my Github repo to publish any and all changes, the dates on every page/note updates to use today's date. 

In order to resolve this I've done a few things. I've since updated my recent notes page so that it automatically updates. Saves me the pain of such a tedious of updating that for every time I make/change a note. 
This was easy as it just involved me FINALLY using the [Dataview](https://github.com/blacksmithgu/obsidian-dataview) plugin. I do want to format this a little bit better, but it's really unnecessary at the moment as other things take priority. 

Like fixing the god damn date on all of my notes.

I've also installed the [Frontmatter Modified Date](https://github.com/alangrainger/obsidian-frontmatter-modified-date) plugin to update the modified date on each note. Which is nice as it lets me know when the last time I made a change to any notes was. It also plays into Dataview, giving me a field that updates on its own and Dataview can pull for the recent notes page.

The extra stuff is whatever. But I seem to be stuck. I'm scouring the discord for any information that would help. 
Looking at the [Modified Date](https://quartz.jzhao.xyz/plugins/CreatedModifiedDate) page I have changed the defaultDateType to modified. And have attempted to change the priority in the 