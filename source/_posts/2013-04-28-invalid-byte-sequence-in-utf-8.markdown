---
layout: post
title: "invalid byte sequence in UTF-8"
date: 2013-04-28 14:30
comments: true
categories: [solved, blogging, errors]
---

I finally made the switch to octopress this week, and when I was
importing some old blog posts, I got this gem of an error message:

    YAML Exception reading 2012-05-28-prefix-search.markdown: invalid byte
    sequence in UTF-8

<!-- more -->
That's surprisingly useless when you're not telling me what line it's
on! The ruby callstack also does nothing! There is literally no other
way to fix this than to bisect the blog post and rebuild the blog
after each change, which currently takes 80 seconds. After a lot of
waiting, I finally naoorwed it down to a single unicode \240
whitespace character that somehow snuck into the text during the
export from tumblr.

Ruby is not scoring any points in my book today.
