---
layout: post
title: "Prefix Search, Part 1: A Challenge!"
date: 2012-05-24 18:35:00
comments: true
categories: [kata, code, algorithms]
---
Algorithms and data structures are fun. The other week, I had the chance to
implement something I needed for a project: Given a large set of strings, find
all the ones that begin with a given prefix. For example, say you have a phone
book, and you want to find all the people whose name starts with Joe. Or a large
list of IP addresses, and you want to find all the ones that start with 192.168.

<!-- more -->
This is a fun problem, because I don't think any popular programming languages
have good data structures to do this. Let me know if I'm wrong, but I can't
think of a naive way to implement this in Javascript or with the STL in C++.

I wrote my own solution in C, based on a paper by D. J. Bernstein. It is super
fast, and has some neat additional properties that I want to write about, but
I'll save that for one of my next posts (have to get this post count up). I'm
putting the resulting code on github for the world, but I'll give you a chance
to think about the problem before I spoil it ;-)

If you are tempted to write your own solution, here's a clever little benchmark
I came up with: Insert all the numbers from 0 to 999,999 into your data
structure (as strings), then find all the ones where the first character is a
'1'. You should get exactly 111,111 matches, and the entire process should
probably take less than a second.
