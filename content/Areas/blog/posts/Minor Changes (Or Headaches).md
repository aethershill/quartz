---
title: Minor Changes (Or Headaches)
modified: 2024-10-07T16:39:39-07:00
creation date: 2024-10-07T04:36:00
created: 2024-10-07T16:33:54-07:00
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
Looking at the [Modified Date](https://quartz.jzhao.xyz/plugins/CreatedModifiedDate) page I have changed the defaultDateType to modified. And have attempted to change the priority in the plugin/lastmod.ts 
Honestly I'm not sure if this is the right area to make the changes. I've tried giving filesystem priority. Did not work.
Currently waiting for the process to resolve so I can see if giving git priority fixes my issue.

Those options didn't work.

BUT I found a solution

I did multiple things, I gave frontmatter priority in lastmod.ts
And then I changed line 54 to 
	`modified ||= file.data.frontmatter["modified"] as MaybeDate`

This worked for the main page. But did not update my recent notes component.

And then I immediately realized that Dataview doesn't automatically render on the page. So my Recent Notes file on the published site, is just a weird comment block. Great.

I realized that the date changed for my [main page](_index) but none of the other pages.
Right now I'm checking to see if pages having a creation date in the frontmatter is affecting the dates. 
This was not, and then I realized that my updated modified plugin is not working. Nevermind.

The plugin is working.

