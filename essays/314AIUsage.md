---
layout: essay
type: essay
title: "My AI Usage: ICS 314"
# All dates must be YYYY-MM-DD format!
date: 2026-05-10
published: true
labels:
  - Software Engineering
  - Artificial Intelligence
  - Reflection
---

## Introduction ##

AI tools have become a normal part of how a lot of software gets written now. In ICS 314 that was true for me too. I used Claude by Anthropic for most of the course, and I used it heavily. That included everything from working through WODs to building the final project.

I picked Claude over other options mostly because it explained things rather than just producing code. When I asked it a question, it usually walked through the reasoning, which made it easier to actually understand what was happening rather than just copying an answer. That said, using it as much as I did came with some real trade-offs that I noticed over the semester.

This essay goes through each part of the course and looks at how I used AI, what worked, and what did not.

## Personal Experience with AI ##

**Experience WODs**

I used Claude on most of the Experience WODs. My usual approach was to try the problem myself first, and then bring in Claude when I got stuck. For the functional programming WOD involving Underscore, I had the right idea but was chaining methods in the wrong order. My prompt was something like:

> Write a function using Underscore that takes an array of student objects and returns only those with a GPA above 3.5, sorted by last name. Explain each method you use.

The explanation helped me understand why the order mattered, not just what the correct order was. The risk I noticed was that I sometimes asked Claude before I had really sat with a problem long enough. It was easy to shortcut the struggle, and some of that struggle was probably useful.

**In-class Practice WODs**

For practice WODs I made a rule for myself to finish the attempt before looking at Claude. Once the timer stopped I would ask Claude to look at what I had written and tell me where I went wrong or what I could have done more simply.

> Here is my solution to the Meteor React practice WOD. What did I do less efficiently and why?

That worked well. Seeing my own approach next to a cleaner one made the differences concrete. Using Claude after the fact felt like getting feedback, which is different from just getting an answer.

**In-class WODs**

I used Claude less on the graded WODs. Mostly I kept it in the background and only asked about something if I hit a specific error I could not read. One time I pasted a broken component and asked:

> Why is this React useState hook not re-rendering my component? [pasted code snippet]

Claude found the problem right away. It was a stale closure issue. I understood the fix but I am not sure I understood why closures go stale in that context. That is probably the honest cost of using AI in timed situations. You get unblocked, but you do not necessarily get the understanding you would have gotten from figuring it out yourself.

**Essays**

I did not use Claude much for essays. When I tried asking it to write a paragraph, the result did not sound like me and did not include the specific things from class that made an essay worth reading. I found it more useful to write something myself and then ask Claude to poke holes in it.

> Here is a paragraph I wrote about the importance of coding standards. Identify any structural weaknesses or unclear claims without rewriting it for me.

That kind of feedback was useful. It pointed out where my reasoning was thin without replacing my voice.

**Final Project**

The final project was where I used Claude the most. Our team built a study group matching app in Meteor and React. I used Claude to think through how to structure the data, debug Meteor methods that were not behaving as expected, and check my code before opening pull requests.

> We have a Meteor collection called StudyGroups. Each document has an array of member userIDs and a subject field. What is the best way to query all groups a specific user belongs to, and what indexes should we define?

Claude gave a solid answer and explained the index reasoning, which I would not have thought about on my own. It did sometimes suggest patterns that did not fit Meteor's reactivity system well, so I had to verify things rather than just trust the output. But overall it was the most useful tool I had for the project.

**Learning a Concept / Tutorial**

This was probably where Claude helped me the most. When I was confused about React's useEffect dependency array, the official docs and Stack Overflow both left me more confused. I asked Claude:

> Explain React's useEffect dependency array like I understand JavaScript closures but have never used React before. Give a real example where getting it wrong causes a bug.

It gave me a before and after example that showed exactly what breaks and why. That clicked in a way that reading docs had not. I used Claude the same way for Meteor's publish and subscribe system and for Mongo query operators. It was a faster way to get a working mental model than documentation alone.

**Answering a Question in Class or on Discord**

I did not use Claude to answer other students' questions. If I knew the answer from my own experience I would share it. If I did not know, I stayed quiet. Using Claude to generate an answer and then passing it off as my own did not feel right. I also figured a classmate asking a question deserved a real human perspective, not something I had just looked up thirty seconds before.

**Asking or Answering a Smart Question**

Before posting a question on Discord, I would sometimes run it by Claude first to see if there was an obvious thing I had missed.

> I am about to ask my classmates why my Meteor subscription is not stopping when the component unmounts. Here is what I have tried. Am I missing something obvious before I post?

About half the time Claude found something I had overlooked and I fixed it myself before posting. The other half it confirmed I had a real problem and I posted the question. That felt like a reasonable use of the tool.

**Coding Examples**

When I needed to understand a method I had never used, I asked Claude for a small working example rather than reading the documentation cold.

> Give me a working example of Underscore's _.groupBy applied to an array of course objects with subject and credits fields. Then show me how _.countBy differs.

Having both methods shown side by side made the difference between them obvious immediately. The examples were small enough to run in the console and test directly. That was faster than reading docs and searching for separate examples.

**Explaining Code**

I used Claude fairly often to explain code I did not write. This came up when reviewing classmates' pull requests and when trying to understand packages we were using in the project.

> Explain what this Meteor publication is doing line by line, and tell me what would happen if I removed the check() call. [pasted code]

The explanations were accurate and usually included things like security implications that I would not have caught on my own. It helped me actually read code rather than just skim it.

**Writing Code**

I used Claude to get a starting point for things I was not sure how to structure. My usual approach was to ask for a rough version, read through it to understand how it worked, and then write my own version from scratch rather than copying directly.

> Write a Meteor method called addMember that takes a groupId and userId, validates both, and pushes the userId into the members array. Include appropriate error handling.

Claude's version handled edge cases I had not thought about, which was useful. The problem I ran into was that I sometimes skipped the rewrite step when I was short on time. Those were the moments I got stuck during code reviews because I could not explain what I had submitted.

**Documenting Code**

For JSDoc comments I used Claude after the code was already written and working. Since the function existed, I was not worried about Claude making things up.

> Write JSDoc documentation for this Meteor method. Focus on param types, return values, and any thrown exceptions. [pasted function]

The output was accurate and saved time. Documenting code is tedious and Claude handled it cleanly. This felt like a low-risk use because it was describing something real, not generating something new.

**Quality Assurance**

Before committing code I would paste files into Claude and ask it to fix ESLint errors. I always asked it to explain each fix rather than just make the change.

> Fix the ESLint errors in this file without changing the logic. Explain each fix so I understand the rule that was violated. [pasted file]

That worked well for linting. For logic bugs it was less reliable. A few times it fixed the reported issue and introduced a different one. I learned to always test the output rather than trust it.

**Other Uses**

I also used Claude when I was stuck and did not know what question to even ask. I would describe the situation in plain language and Claude would usually help me figure out what I was actually trying to solve. That was useful more often than I expected. It also helped me compare design choices, like asking why Meteor handles state differently than a plain React app would, which gave me context the course materials did not always cover.

## Impact on Learning and Understanding ##

Claude made it faster to get through confusing topics. Things that might have taken me a day of reading and searching became clear in an hour of back and forth conversation. That was genuinely useful, and it meant I could spend more time on the project work where understanding actually mattered.

In some places it hurt. The clearest example was timed WODs. When I was used to having Claude available to look things up instantly, I had less practice holding the problem in my head and working through it without help. That showed up a few times when I froze during graded work because I had not built the habit of debugging on my own.

The other place it hurt was code I did not rewrite myself. If I took Claude's output directly without understanding it, I could not explain it later. That happened more than I would like to admit, and it was always obvious in the moment when someone asked a follow-up question.

I came into the course knowing almost no JavaScript and left able to build a working Meteor app. AI helped with that, but the parts that stuck were the parts I actually worked through, not the parts I generated.

## Practical Applications ##

I did not do the HACC or any outside projects this semester. I did use the same habits from ICS 314 on a small personal project I built to practice the Meteor patterns we were learning in class. It was a basic task tracker, nothing complicated.

Working on that without course deadlines changed how I used Claude. I asked more open-ended questions because there was no WOD description telling me what the answer should look like. That was actually harder. Claude is most useful when the problem is specific. When I asked something vague like whether my design was good, the answers were not very helpful. It works better when you already know enough to ask a concrete question.

## Challenges and Opportunities ##

The biggest problem I ran into was that Claude was sometimes wrong and did not signal that it was uncertain. Early in the semester it gave me an answer about the Meteor Accounts package that described an older version of the API. I used it, it broke, and I had to trace back what happened. After that I made a habit of checking anything Claude described against the actual documentation before using it.

The other challenge was dependency. At some point I realized I was reaching for Claude before I had actually tried anything myself. I had to put a rule in place to attempt problems for at least ten minutes on my own before asking. That helped.

On the other side, I think there is room for courses like ICS 314 to be more explicit about how to use AI well. Not just allowing it or restricting it, but teaching how to ask good questions, how to check the output, and how to know when the tool is not reliable. That is a skill that would actually carry into a job.

## Comparative Analysis ##

The traditional way to learn programming is to read, get stuck, debug, and eventually figure things out. That process is slow, but it builds real intuition. You remember things you had to fight for.

AI makes it much faster to get to a working answer. The risk is that getting to the answer faster does not always mean you understand it more deeply. It can mean you have seen more things without really knowing any of them.

What worked for me was switching between the two. I would use Claude to get oriented on something new, then put it away and try to apply the concept on my own. When I got stuck again, I would bring it back. That cycle worked better than either extreme. Using AI for everything left gaps in my understanding. Avoiding it entirely would have slowed me down more than was useful.

## Future Considerations ##

AI coding tools are going to keep getting better and more integrated into development environments. That is not a question. The question for a course like ICS 314 is what to actually teach students about using them.

Right now most courses either ignore the topic or just say AI is allowed. Neither of those is very useful. What would actually help is teaching students how to write a prompt that gets a useful answer, how to verify output before trusting it, and how to recognize when an AI is outside its reliable knowledge. Those are practical skills that will matter for a long time regardless of what specific tools exist.

Assessment is also going to need to change. Take-home work is hard to evaluate in a world where AI can write most of it. Projects where students have to explain their code out loud, or where the process is part of the grade, make more sense. That is where understanding shows up and shortcuts do not.

## Conclusion ##

I used Claude heavily in ICS 314 and it helped me get through a lot of material I would have struggled with otherwise. It was most useful for learning concepts, explaining unfamiliar code, and getting unstuck on specific problems. It was least useful when I let it replace the thinking I should have been doing myself.

The thing I would tell someone starting the course is to use AI as a tutor, not an answer machine. Ask it to explain things. Ask it to find the problem in your thinking. Ask it to show you an example you can actually run. But write your own code, and make sure you can explain it. The grade matters less than whether you actually understand what you built.

For the course itself, I think making AI use visible would help. If students had to document what they asked and what they did with the answer, it would force more honest engagement with the tool and make it easier to see where people are relying on it in ways that hurt their learning.
