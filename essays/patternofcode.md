---
layout: essay
type: essay
title: "The Patterns in Code"
# All dates must be YYYY-MM-DD format!
date: 2026-04-30
published: true
labels:
  - Design Patterns
  - Software Engineering
  - System Design
---

## What Are Design Patterns? ##

Design patterns are not specific lines of code. They are reusable, named solutions to problems that keep coming up in software development. At first, the concept can feel abstract. Why give a name to something you could just figure out on your own? The answer is that naming a solution gives your team a shared vocabulary. When someone says *Observer* or *Singleton*, everyone immediately understands the intent, the structure, and the tradeoffs - before a single line of code is written.

The term was popularized by the "Gang of Four" in their 1994 book *Design Patterns: Elements of Reusable Object-Oriented Software*, which organized 23 patterns into three families: **Creational** (how objects are created), **Structural** (how objects are composed), and **Behavioral** (how objects communicate). Decades later, these still apply directly to modern web development.

<img width="400px" src="../img/bowlletins-home.png" class="img-thumbnail">

## Design Patterns in Bow-lletins ##

My final project, [Bow-lletins](https://bowlletins.vercel.app/), is a campus bulletin board web app for UH Mānoa where students can find jobs, events, study groups, and internships. Building it is where I first started recognizing these patterns in my own code.

The **Composite** pattern shows up throughout the React component tree. A `FlierCard` and a `FlierGrid` full of `FlierCard` components are both just components - the tree can be as deep as needed, and swapping one node does not break the rest. When we added an RSVP button to `FlierCard`, it appeared everywhere automatically.

The **Observer** pattern appears in the search feature. The search bar is the subject, and any component that cares about the current query - the flyer grid, the category filter - is an observer. React's Context API handled the subscriptions, so no component needed to know about any other. They all just watched for changes and updated on their own.

The **Factory** pattern came up when we needed four different card layouts for four different categories. Rather than scattering conditionals across the codebase, a single `FlierCardFactory` accepts a category string and returns the right component. Adding a new category means updating one file.

The **Singleton** pattern appeared on the backend. Creating a new database connection for every request is expensive, so our database client is initialized once and shared across the app. Node's module caching enforces this automatically.

## Patterns as a Shared Language ##

I did not sit down with a list of patterns and decide which ones to use. They emerged from real problems, and I only recognized them by name afterward. That is actually what makes design patterns valuable - they describe solutions that developers naturally reach for, and naming them makes it easier to talk about, teach, and revisit those decisions later. Understanding them has made me more aware of the structure in my own code, and better at explaining that structure to others.

*Used ChatGPT to help with grammar and punctuation.*
