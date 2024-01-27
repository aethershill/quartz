---
title: Structuring the Garden
enableToc: true
tags:
  - Blog
  - Blog/Published
---

## First Thoughts
Some of my first thoughts on how I want this to look:

I really like the Map of Content from https://www.ssp.sh/brain// so figuring out how to do something similar would be ideal. 

I also want to include a blog hyperlink in the header, to make it easier to access. 

In order to do these two things, I need to figure out how to properly customize/format inside of [[Areas/blog/posts/Humble Beginnings|Humble Beginnings]]/[[Resource/wiki/web design/Quartz|Quartz]]. I believe this requires me to learn more about [[Resource/wiki/web design/Hugo|Hugo]]?

Currently reading: https://gohugo.io/content-management/taxonomies/ on [[Resource/wiki/web design/Taxonomies|Taxonomies]]. 

Appears that taxonomies would be useful for the wiki, but not for easier access to blog/posts. ^[This turned out to be a dead end. Did not end up needing to go into taxonomies at all, maybe at a future date]

## Temporary measures
My plan for accessing the blog is to just have a link on my main page. 
Hugo allows you to create index pages if you title the file `_index`. 

The index shows all pages in the same folder or below it so I don't have to manually add each new blog post to a directory (or MoC). The only downside to note is that blog posts are in alphabetical order rather than in chronological order.^[Realized after that posts are being ordered chronologically by most recently updated, which I think is fine.]
A simple solution for this is to add dates to all the file names.

The next problem that arose was that using [[Resource/wiki/productivity/Obsidian|Obsidian]] I am able to easily link notes together. But linking directly to the index file makes it look ugly and unintuitive. It creates a hyperlink that says `_index`, which is functional. But not ideal.
initially, I attempted to use Hugo markdown to create a hyperlink named Blog but for some reason the file path didn't work. I am unsure if it doesn't because of some user error or if there is something else going on underneath the hood. 

## Aliases
The next thing I figured out was that where hugo stores markdown meta info, I can create taggable aliases. 
In my index page for the blog posts the beginning of my post looks like this: 

```
title: "Blog"
aliases:
- Blog
```

This works with Obisidian, so using Obsidians linking feature I am able to create a link to `/Areas/blog/_index` with ease.

## Internal links in tables not working?
Thinking that "surely my issues are almost over", I was wrong found an issue with tables. I am able to create tables.
I created a table for my Map of Content, using that look I mentioned earlier in this post for its simplicity.
Linked to all folder indexes I wanted mapped so far.
And then when the page rendered after being published, it looked like internal links (at least the way Obsidian does links, markdown and wikilinks) are broken when inside tables. 

Initially linking to the index files, which works in Obsidian, led to the link just being broken. 
`[[Resources/wiki/pkm/_index.md]]`
First thought was to try to drop the .md and see if this worked. 
`[[Resource/wiki/pkm/_index]]`
This succeeded in rendering as a link, but the internal link was (apparently) broken and would otherwise lead to nowhere.

After looking at the links for categories I could reach using Quartz's built in search, I mistakenly tried: `[[Resource/wiki/pkm/_index/#]]` 
Looking back, the reason why this didn't work immediately comes to mind but stumped me for a solid 10-15 minutes. 
In the end, linking to the folder itself was the solution the entire time. 
Linking to the folder will automatically direct you to the index page (assuming you've created one) with a clean URL structure. 
This extra understanding leads me to think I can drop the Aliases from the blog post and just link to my blog folder, save a few bytes or kb.

As a little test, I decided to try remove index.md from Web Design to see if linking to the folder would still work. As I should have remembered from when I first started messing around with websites, no.

