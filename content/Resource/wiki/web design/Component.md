---
title: Component
modified: 2024-10-23T12:02:49-07:00
created: 2024-10-23T12:01:07-07:00
---
A component is "undefined" if it has a [delimiter]] and the delimiter does not appear in the URI.

Scheme and path are always defined. 

A component is "empty" if it has no characters.
Scheme component is never empty. 

The authority component is made up of subcompontents.

` authority = [userinfo "@"] host [":" port]`
