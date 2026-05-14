---
layout: essay
type: essay
title: "My Software Engineering Experience"
# All dates must be YYYY-MM-DD format!
date: 2026-05-13
published: true
labels:
  - Software Engineering
  - Reflection
---

## More Than Web Development ##

When I started ICS 314, I assumed it was mostly about learning how to build websites. By the end of the semester that assumption was clearly wrong. The web stack we used was just a vehicle. The actual content of the course was software engineering, and a lot of what I learned applies to building any kind of software, not just web applications. Four concepts stood out to me as genuinely transferable: design patterns, configuration management, ethics in software engineering, and coding standards.

## Design Patterns ##

A design pattern is a reusable solution to a problem that comes up often in software development. It is not a piece of code you copy and paste. It is more like a named strategy that developers recognize and can apply to similar situations in different contexts.

From in and outside class, I encountered patterns like the Observer pattern, where one object notifies others when its state changes, and the Singleton pattern, which ensures only one instance of something exists at a time. These showed up in how Meteor handles reactive data, but the patterns themselves are not specific to Meteor or to the web.

If I were building a mobile app, a desktop tool, or even a command-line program, the same patterns would apply. A game tracking player score changes would benefit from the Observer pattern. A configuration manager that should only ever have one instance loaded at a time would use Singleton. The names and concepts travel across domains because the underlying problems they solve keep showing up in software regardless of what you are building. Learning to recognize the pattern is more valuable than memorizing a specific implementation.

## Configuration Management ##

Configuration management is the practice of tracking and controlling changes to a software system over time. In this course that mostly meant using GitHub, branching for new features, reviewing code before merging, and keeping a clean commit history.

It is easy to think of this as a web development thing because that is the context where I learned it. But configuration management matters anywhere software is built by more than one person, or by one person over a long period of time. A data science team working on a machine learning pipeline needs to track which version of the model was trained on which dataset. A game studio needs to manage changes to a codebase across dozens of contributors without breaking each other's work. A research team writing simulation software needs to be able to reproduce results from six months ago.

The specific tools might differ, but the discipline is the same: you track what changed, when, and why. You do not work directly on the main codebase when you are trying something new. You review changes before they go in. Those habits apply to any collaborative software project, not just one using Meteor and React.

## Coding Standards ##

Coding standards are agreed-upon rules for how code should be written and formatted within a project. That includes things like how variables are named, how functions are structured, how long lines should be, and how to handle errors consistently.

In ICS 314 we used ESLint to enforce standards automatically. At first it felt like busywork, fixing spacing issues and import ordering that seemed trivial. Over time I realized the point was not the specific rules. The point was consistency. When everyone on a team writes code that looks roughly the same, it is much easier to read each other's work, catch bugs during review, and hand off tasks without friction.
<img src="../img/cat-typing.gif"
     class="img-thumbnail float-end ms-3 mb-3 mt-3"
     width="400px">
This matters just as much outside of web development. A team writing embedded software for a medical device needs coding standards more than most, because inconsistent code in that context can have serious consequences. A group of data engineers writing ETL pipelines benefits from standards that make it obvious when something is wrong. The tools used to enforce standards might be different, but the underlying value of readable, consistent code does not change based on what kind of software you are building.

## Ethics in Software Engineering ##

Ethics in software engineering means thinking carefully about the impact your software has on the people who use it and on the people it affects, even if they never use it directly. It means asking not just whether something works, but whether it should be built, and how it should be built.

In this course we read the ACM Code of Ethics and talked about things like privacy, accessibility, and the responsibility developers have to be honest about what their software does. Those conversations were grounded in web app examples, but the questions they raised go much further.

A software engineer working on facial recognition technology has to think about bias and who gets harmed if the system makes mistakes. A developer building a recommendation algorithm has to think about what the system is actually optimizing for and what effects that has on users. Someone writing software that controls physical systems, like medical devices or autonomous vehicles, is making decisions that directly affect people's safety. In all of these cases, the technical work is inseparable from ethical responsibility. Knowing how to write clean code is not enough. You also have to be willing to ask whether what you are building is actually good.

## Conclusion ##

From how I see it, the web application we built was the project. The software engineering concepts behind it were the education. Design patterns, configuration management, coding standards, and ethics are not web-specific ideas. They are ways of thinking about software that will be useful in any technical role I end up in, regardless of the tools or the domain. That is probably the most useful thing I am taking out of this course.

Overall though, I'm glad what I got of this course and can't wait to see where else I can utilize these skills.

*Used Claude to help with punctuation and grammar*
