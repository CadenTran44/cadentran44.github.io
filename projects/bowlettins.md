---
layout: project
type: project
image: img/bowlletins.png
title: "Bow-lletins"
date: 2026
published: true
labels:
  - Final Project
  - React
  - Prisma
  - Team Project
summary: "My ICS 314 Final Project"
---

<img width="700px" src="../img/bowlletins_home.png" class="img-thumbnail">

## Overview ##
 
Bow-lletins is a full-stack web application built for University of Hawaii at Manoa students. Campus life at UH is active, but finding out about it is harder than it should be. Events get posted to Instagram, job opportunities show up in Discord servers, and study group flyers get pinned to physical boards that most students walk past without noticing. Bow-lletins puts everything in one place with a searchable interface built around the familiar metaphor of a cork board.
 
Students can create and browse flyers organized by category, including jobs, campus events, study groups, and internships. They can like and save postings, RSVP to events, and see what is happening across campus in a single feed. Administrators have a dedicated dashboard for managing content and users.
 
The stack is Next.js with the App Router, PostgreSQL for the database, Prisma as the ORM, React for the UI, and Bootstrap 5 for styling.

## What I Contributed ##
 
My primary contribution was the overall design and visual identity of Bow-lletins. The cork board metaphor was central to everything. Rather than building a generic feed with cards, I wanted the application to actually feel like a bulletin board — something tactile and familiar that students would immediately understand. That meant establishing a consistent visual language across the entire app, including the warm cork-toned backgrounds, the pinned card aesthetic, the handwritten-style typography for decorative elements, and the color palette built around UH Manoa's greens.
 
I handled the global styling system, setting up the CSS custom properties and Bootstrap overrides that gave the application its consistent look. This included defining the spacing, border radius, shadow depth, and color tokens that every component pulled from. Having that foundation in place early meant the team could build new pages without making visual decisions from scratch each time.
 
I also designed and built several of the key UI sections, including the landing page hero, the category cards, and the navigation bar. The landing page in particular went through several iterations. Getting the layout to feel balanced between the hero content and the sign-in form while keeping the cork board background readable underneath took more time than expected, but it became the visual anchor for the rest of the site.
 
Beyond individual components, I worked on making the design coherent as the application grew. When new pages were added, I reviewed them for consistency and adjusted styles where things drifted from the established system.

 
## What I Got Out Of It ##
 
Building Bow-lletins taught me what it actually looks like when multiple people work on different parts of the same codebase at the same time. The Prisma schema is a shared contract, and a change to one model can break things for everyone. Learning to make deliberate changes to that schema and communicate them clearly through GitHub issues was one of the most practical lessons of the project.
 
I also got real experience with Issue Driven Project Management. Moving from loose assignments to discrete issues with clear owners and definitions of done made the work trackable and helped catch blockers before they became larger problems. That workflow is something I plan to carry into future team projects.
 
On the technical side, I came away with a better understanding of how Next.js Server Components interact with the Prisma client, how session data flows through NextAuth.js into page components, and how to structure API routes that handle both validation and database writes in a clean and predictable way.

Our Project: [Bow-lletins](https://bowlletins.github.io/)