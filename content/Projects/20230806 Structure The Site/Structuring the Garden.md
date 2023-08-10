---
title: "Structuring the Garden"
tags: 
- blogging
---

## First Thoughts
Some of my first thoughts on how I want this to look:

I really like the Map of Content from https://www.ssp.sh/brain// so figuring out how to do something similar would be ideal. 

I also want to include a blog hyperlink in the header, make it easier to access. 

In order to do these two things, I need to figure out how to properly customize/format inside of [[Areas/blog/posts/Humble Beginnings|Humble Beginnings]]/[[Resource/wiki/web design/Quartz|Quartz]]. I believe this requires me to learn more about [[Resource/wiki/web design/Hugo|Hugo]]?

Currently reading: https://gohugo.io/content-management/taxonomies/ on [[Resource/wiki/web design/Taxonomies|Taxonomies]]. 

Appears that taxonomies would be useful for the wiki, but not for easier access to blog/posts.^[This turned out to be a dead end. Did not end up needing to go into taxonomies at all, maybe at a future date.]

My temporary measure for accessing the blog is to just have a link on my main page to the blog. 
Hugo allows you to create index pages if you title the file `_index`. 

The index shows all pages in the same folder or below it so I don't have to manually add each new blog post to a directory. The only downside to note is that blog posts are in alphabetical order rather than in chronological order. 
A simple solution for this is to add dates to all the file names.

The next problem that arose was that using [[Resource/wiki/productivity/Obsidian|Obsidian]] I am able to easily link notes together. But linking directly to the index file makes it look ugly and unintuitive. It creates a hyperlink that says `_index`, which is functional. But not ideal.
initially, I attempted to use Hugo markdown to create a hyperlink named Blog but for some reason the file path didn't work. I am unsure if it doesn't because of some user error or if there is something else going on underneath the hood. 

The next thing I figured out was that where hugo stores markdown meta info, I can create taggable aliases. 
In my index page for the blog posts the beginning of my post looks like this: 

```
title: "Blog"
aliases:
- Blog
```

This works with Obisidian, so using Obsidians linking feature I am able to create a link to `/Areas/blog/_index` with ease.

The next problem arises with tables. I am able to create tables, but it looks like internal links (at least the way Obsidian does links, markdown and wikilinks) are broken when inside tables. 