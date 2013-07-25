---
layout: page
title: Conducting Effective Code Reviews
categories: []
type: page
published: true
author: glenn
---

**Written by:** Glenn Burnside, Director of Software Development, Headspring

## You’re Doing Your Code Reviews Wrong!

Well, not YOU, of course. YOUR team’s code reviews, I’m sure, are pleasant, productive engagements where everybody leaves feeling good about the results. They happen early and regularly in the development process, the goal of the review is well understood, and you wouldn’t dream of shipping a line of code that hadn’t been through your review process. Your team loves doing them, and you don’t worry about who does the review because you’ve got a consistent standard that your whole team agrees with. You’re just reading this article because there’s this other team in the building that you think would benefit from reading it, and you’re going to forward it to them when you’re done reading.

I’m with you. Personally, I’ve never sat around a meeting table with 15 other developers, all checking their email, while one poor sacrificial lamb walked us through a line-by-line explanation of code in “Representative changeset XYZ” the day after we put it into production. I’ve never been told (or said!) “That’s good feedback, but we don’t have time to re-test those changes before the release date.” And I’ve never, ever had an hours-long debate about where our braces should go.

Really.

Let’s face it, nobody likes doing code reviews the way they always get done. They’re boring and unproductive. They demotivate the development team. They get used as weapons. They make us feel bad about our code but they don’t help us improve. There’s got to be a better way! I think the problem starts though with this: We all agree we should be doing code reviews, but nobody can remember why. That’s why I think you should always start there:

## Know the Goal

First off, if your team doesn’t know why they’re doing code reviews, they won’t get anything from it. So 
why do we do code reviews?

* Ensure a consistent dialect in the codebase

* Preserve architectural integrity

* Ensure features do what they’re supposed to

* Catch bugs

* To teach

* To learn

It’s virtually impossible to argue with these goals. Who wouldn’t want these things? Most people’s objection to code reviews aren’t because of these goals, it’s because their current process for doing reviews doesn’t actually achieve them. That’s what the rest of this list is about.

##Code Reviews are the First Quality Gate

Code should never pass review the first time. There’s always something that can be improved. We all know that it’s cheaper to fix a bug in development than in production. But did you know that formal code reviews have been shown to find twice as many defects as other forms of application testing? It’s true! Good developers can read the code, and just see the bugs. And usually, those are the kinds of bugs for 
which you’d never have written a test.

Am I suggesting you stop writing unit tests? Of course not. I’m suggesting that you, as the developer of a new feature, would benefit from a pair of fresh eyes reviewing your code and your tests, because the bug you don’t see is also the one that’s missing a test case. Besides, how do you write a test that proves that your implementation fits within the application’s architectural model? Even if you stuck all your data access code smack in the middle of your business objects, and your application is supposed to be using a Repository pattern everywhere, I bet you could make all your tests pass. But your teammates would probably have you tarred and feathered if your feature went into production that way.

> Code reviews are your team’s first defense against design and implementation mistakes.

## Braces and Spacesare Boring

If your code review feedback never rises above the level of “we always put braces around if statements, even if it’s one line long.” then you’re wasting your time. I really, really don’t care if your team uses sameline braces, separate-line braces, or no braces at all. I don’t care if you left-align your variable names. I don’t care if you prefix instance fields with an underscore, or an “m”, or if you require all field references to be “this.”-prefixed. I’ve seen teams where code reviews never got past this level of inspection. And I really, really, really don’t care whether you standardize on 2, 3, or 4-space tabs.

I do care that you all agree how you’re going to do it. Sit down together once, figure out what hills you’re going to die on, and write it down. Give everyone a copy. Make sure that every time you have a code review, the code meets all the formatting standards. Allow no exceptions. Pick your dialect and enforce it. Any standard is better than no standard at all. With all the time we’ve all spent reformatting “other peoples’ code” to look the way we like we probably could have cured world hunger or something.

Tools like CodeRush, ReSharper, and StyleCop make it simple to not only have a formatting standard, but to ensure that everyone can automatically follow it. On some of my teams, we created a ReSharper formatting and code cleanup template, and shared it with the team. We all developed a habit that before you checked in a file, you ran the standard cleanup on it. Automating this nit-picky, boring stuff meant we could spend more time on interesting things during review, like gauging the code’s maintainability and separation of concerns.

> Team-wide shared code ownership means you have to put your personal preferences aside.

## The End of the Project is Too Late

If your code reviews happen right before you ship, or - even worse - afterwards, you’re wasting your 
time. I’ve NEVER seen a team take action on code review feedback when it was done right before a ship 
date, or by reviewing last release’s code at the beginning of vNext. Here’s what happens instead:

* So, here’s feature XYZ...

* You know, you could refactor all the email templating out to a separate class in the business services layer. That’d make a lot of these unit tests simpler to understand, and we could test all the email creation without actually sending messages on the test server.

* That’s true, but we don’t have any time for that. We’ll just add it to the backlog.

* ...6 months pass...

* So, uh, Ms. Product Owner, we’d like to defer those two features so we can refactor our email emplating out of the Floozit class...

* Ms. Product Owner laughs and laughs and laughs at the silly developers and kicks them out of her office.

This is the very definition of technical debt. If you’re not going to act now on what you learn, you will never change the quality of the code you produce. Old habits will persist, and you’ll eventually stop inspecting your code at all, because the whole team will know it’s an exercise in wishful thinking.

> Code Reviews are feedback. Schedule enough capacity to act on that feedback.

## Good SCM Makes Reviews Easier

If your developers are all checking in changes on the same line of code, how do you know what to review? How do you inspect the sum total of changes in source control that make up a particular feature? To what do you compare it? When all your developers are working in a single branch in source control, you usually can’t easily inspect all the code for a certain deliverable. This scenario is where I usually find people inspecting “representative changes”. I look at it this way - if one checkin has issues, odds are that most of your other checkins do too. If you inspect 1 changeset out of twenty, you’re only catching 5% of all the issues you should be catching. That’s not even worth the effort.

I’m a big believer in feature branches. I know I’m speaking heresy against Martin Fowler when I say that, but I bet he’s not reading this anyway. In my experience, isolating feature development in separate branches does a lot of good:

* Features can be pulled from a release by the act of not committing them to the trunk

* You have a full linear history in source control of the changes related to a particular feature

* Knowing what code to review is trivial

Why that last point? Think about this - if all the commits in a branch are for a single feature, then the code that makes up that feature is the difference between the trunk tip and the branch tip. If you want to see the full set of work that went into that feature, just diff the branch with the trunk. There’s your code to review, handed to you on a platter by your source control system.

Of course, I’m assuming you’re merging changes down from your trunk and resolving conflicts regularly, but that’s probably a post for another day.

> Effective code reviews require simple access to all the changes to review. It’s easier to review all the changes together than to review them incrementally.

## Pair Programming Doesn’t Replace Code Reviews

The previous section discussed the many benefits of agile software development. However, to accept Pair programming is a valuable practice. You can get a lot of value from a second set of eyes on your work while you’re producing it. Two heads are better than one and all that. I’ve even heard it called “real-time code reviewing”. That’s where I draw the line. We’re not exactly the first industry to decide that sometimes collaboration is a good thing. In fact, I’ve heard that sometimes, two authors will team up, and actually write a book together. You know what else I’ve heard? They still have an editor read through the result. Pair programming can certainly lead, in many cases, to a better design, and a higher quality resultant implementation. If you’ve got two really strong people building something together, maybe the code review feedback on their work doesn’t uncover as many opportunities for improvement. But those two developers still benefit and grow in their craft from the feedback they do receive.

> Regardless of team practices around pair programming, a separate review activity reveals opportunities for improvement.

## Review Feedback is a Spectrum

If your code reviews are an all-or-nothing, pass/fail proposition, or if the same code keeps coming back for review three or four times, you’re wasting your time. This is still a subjective activity, and you’ve got to draw the line somewhere. Good-enough code in production is better than perfect code in a feature branch. There comes a day when you need to stop perfecting your ViewModel projections and just
ship it.

One technique I find useful for code reviews is providing feedback as a MoSCoW list. I picked this up from a project manager friend of mine several years ago, but I’ve found it very useful in prioritizing code review results. “MoSCoW” is an acronym that stands for “Must, Should, Could, Won’t”. If you can denote all your code review feedback into one of those four categories, then the developer has an opportunity to match their response effort to the priority of the feedback. It also makes it possible to make tradeoffs for schedule constraints without sacrificing everything. I look at these four items like this:

* **Must:** This feature isn’t shipping until this is fixed

* **Should:** If you don’t do these, and resubmit for review, you should have trouble sleeping tonight.

* **Could:** Do these if time and budget allow. If time and budget don’t allow, don’t worry about them.

* **Won’t:** I had a crazy idea about how to redo the whole thing, and I wanted to share it with you. Interesting, but not actionable.

> Code reviews can get out of hand. Don’t let them become a deterrent to delivery

## The Code Review Action Plan

So, that’s all well and good. But what are you going to tell that other team in the building, the ones for whom you’re so kindly gathering all this information? Well, you can share with them my simple, easy-tofollow, patent-pending, Glenn Burnside Code Review Action Plan!

1. If you’re not conducting code reviews on every feature you put into place, start now. Agree as a team that this is a valuable investment of your time and energy.

1. Lay out your team coding standards. Use a tool like ReSharper or StyleCop to enforce them.

1. Leave 5-10% of the total estimated development time for conducting and responding to code review feedback.

1. Have every deliverable reviewed by a senior team member.

1. Follow MoSCoW guidelines for organizing feedback.

1. Give the whole team access to all code review feedback. Odds are that somebody else just made the same design mistake you did.

Once you’ve got that up and running, you can start looking for ways to streamline the process with additional tooling, feature branches, and whatnot. But the first step is to start doing them, and start acting on the feedfback.

Now go tell the team down the hall.
