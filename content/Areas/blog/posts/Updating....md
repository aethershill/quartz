---
title: Updating...
tags:
  - Blog
  - Blog/Published
modified: 2024-10-13T14:44:40-07:00
created: 2023-11-28T03:58:28-08:00
---

Updating my Garden is a little bit of a pain. 

I've added a lot of one off ideas in my inbox but fell behind on maintenance/updates for [Quartz](Resource/wiki/web%20design/Quartz.md). 
While I was "distracted," Quartz 4.0 was released and I felt it was probably best to stay up to date.

Lots of things changed.

I'm still learning quite a bit and attempting to follow the [Migration Guide](https://quartz.jzhao.xyz/migrating-from-Quartz-3) did not work out for me. 
I had no motivation towards troubleshooting this, so I opted for a fresh install and copied my content over. 
I'm not sure what kind of repercussions this will have, I assume it will mostly be configuration but that will be seen.

All that I was learning with Hugo is no longer necessary. 
Hugo was removed which is fine, this will give me the opportunity to learn Node(?). 

One of such issues was the solution to creating a Blog page that I detailed in [Structuring the Garden](Areas/blog/posts/Structuring%20the%20Garden.md) no longer works. It looks like a simple fix though, linking to the /posts/ subfolder seems to generate an index without being specified. 

10/22/23 - 
Coming back to things I've realized a few things.
Without an `_index` page, the file structure for folders becomes apparent in a very ugly way. 
As such, I decided to reimplement those pages for all folders. 
As of the moment, Aliases appear to be useless (for my use case) as page title does most of the heavy duty lift.

I for the most part have things where I want them and just have to continue creating notes/content. 