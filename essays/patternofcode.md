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

I used to think design patterns were specific lines of code, but then I reliezed they're not. They are reusable, named solutions to problems that keep coming up in software development. At first, the concept can feel abstract. Why give a name to something you could just figure out on your own? The answer is that naming a solution gives your team a shared vocabulary. When someone says Observer or Singleton, everyone immediately understands the intent, the structure, and the tradeoffs, before a single line of code is written.

I did some research and found that the term was popularized by the "Gang of Four" in their 1994 book *Design Patterns: Elements of Reusable Object-Oriented Software*, which organized 23 patterns into three families: Creational (how objects are created), Structural (how objects are composed), and Behavioral (how objects communicate). Decades later, these still apply directly to modern web development.

## Design Patterns in Bow-lletins ##

My final project, [Bow-lletins](https://bowlletins.vercel.app/), is a campus bulletin board web app for UH Mānoa where students can find jobs, events, study groups, and internships. As the project grew, it became clear that without some kind of structure, the codebase would get pretty messy fast. That is where design patterns became useful in practice rather than just in theory.
<img src="../img/gangof4.png"
     class="img-thumbnail float-end ms-3 mb-3 mt-3"
     width="400px">
 
One of the most visible patterns was definitely the component-based design. Bow-lletins has several content types like job listings, campus events, study groups, and internships. Each needing its own card layout. Rather than copy-pasting similar UI structures and adjusting them for each case, we centralized card creation so that a single point in the code determined which component to render based on the content type. This made it easy to update a card's behavior or appearance without touching every page it appeared on.
 
The search feature also relied on a pattern, even if it was not labeled as one at the time. The search bar needed to drive updates across multiple parts of the page - the list of results, the active category filter, and the result count. Instead of wiring each of those directly to the input, we kept the query in a shared context so any component could subscribe to it and update independently. That separation kept each component focused on its own job rather than needing to coordinate with everything else.
 
On the backend, we avoided creating a new database connection on every request, which would have been wasteful and unstable. Instead, a single client instance was initialized once and reused throughout the application. It is a simple idea, but it solves a real problem and keeps resource usage predictable.

## Patterns as a Shared Language ##

I of course, did not sit down with a list of patterns and decide which ones to use. They emerged from real problems, and I only recognized them by name afterward. That is actually what makes design patterns valuable in my opinion, they describe solutions that developers naturally reach for, and naming them makes it easier to talk about, teach, and revisit those decisions later. Understanding them has made me more aware of the structure in my own code, and better at explaining that structure to others.

*Used ChatGPT to help with grammar and punctuation.*
