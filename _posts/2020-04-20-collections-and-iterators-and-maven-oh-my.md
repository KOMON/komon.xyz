---
layout: post
title: Collections and Iterators And Maven, Oh My!
date: 2020-04-20
description: 'In which: We learn to make for-each loops go'
img: undecided.jpg
tags: [learning-in-public,java,collections]
---

### What's up?

Whew, it's been about 2 weeks since my last blog post, and what a busy time I've
been having! I admit that I haven't been spending as much time as I'd have liked
to on this project. Turns out that in these troubled times and with an
8-month-old baby I have less time and energy than I would normally attribute to
myself.

But, that's not to say I've done nothing! I have plenty of notes to distill into
this post, and I've been learning quite a bit about the Java workflow I've been
building with Maven.


### Collections API, Ahoy

So, to start off my exploration of core Java APIs I delved into Collections.
Now, collection classes as a topic aren't new to me, I've used plenty of
different PHP implementations of various collection data structures, and
implemented many types of collections myself in C++ back in my early CS
education.

But, being one of the core APIs of the language, I was determined to really
start at the top with the `Collection` interface and wander my way around as I
found fun things to implement myself.

Today we'll be looking at `Collection` in general, as well as the `Iterator` and
`Iterable` Interfaces. We even have some sample code to look at.

### What is a `Collection` anyway?

The `Collection` interface is the root of the collection hierarchy, and all
collection types will implement `Collection` either directly or through one of
its sub-interfaces. A `Collection` embodies the idea of a container for multiple
objects. An implementation of `Collection` supports a few broad categories of
operation:

- Inserting items into the collection
- Removing items from the collection
- Querying the collection for membership of an object
- Measuring the size of the collection

