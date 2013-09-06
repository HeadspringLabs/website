---
layout: page
title: The Agile Difference
date: 2013-09-06 17:06
sharing: true
footer: true
description: Delivering Quality Software Predictably Using Agile Project Management and Extreme Programming Engineering Practices
categories: []
type: page
published: true
author: kevin
---

**Delivering Quality Software Predictably Using Agile Project Management and Extreme Programming Engineering Practices**

**Written by:** Kevin Hurwitz, Chief Architect, Headspring


## Introduction

The first edition of a landmark study, aptly named the “Chaos Report”, was released in 1995 by the
Standish Group and outlines the failed state of custom software development at that time. The study notes that almost one-third, or 31.1% of all software projects were cancelled before they were ever completed. In addition, over half, or 52.7%, of the projects cost at least 189% of their original budget. Of all the projects included in the survey, only 16.2% were delivered on time and on budget. Even amongst these “winners”, a significant percentage was released with only a fraction of the planned functionality.

When the “Chaos Report” was released again in 2005, the results were much better, but still far from remarkable. The total failure rate had dropped to 15%, while the project success rate had more than doubled to 34%. The remaining 51% of projects were considered “challenged” – they were either delivered late and over-budget, or on time with critical features missing.

When the 2005 study was released, Standish Chairman Jim Johnson offered his explanation of the improvement:

> “The primary reason is the projects have gotten a lot smaller. Doing projects with iterative processing as opposed to the waterfall method, which called for all project requirements to be defined up front, is a major step forward.”

Clearly, the increasing acceptance of Agile software development is a positive advancement. However, these dramatically improved figures still mean there is only a one in three chance a custom software implementation will meet stakeholder expectations. In addition, there is almost a one in six chance that the money invested in a custom software project will provide no return on investment. As the project size increases, the chances of marginal and absolute failure become even greater.

To combat this disturbing trend, Headspring Systems has dedicated itself to becoming a pioneer in the application of the Agile development methods, and software requirement and design best practices that are revolutionizing the way high quality software is developed. These best practices have strong synergies with Agile and with one another. When applied in concert by leading IT professionals, these best practices enable Headspring Systems to predictably deliver outstanding value to our clients.
To better understand the Agile Difference, it is important to understand more about why software projects fail.

## Why Custom Software Projects Fail

Software projects can fail for the same reasons that any large capital project can fail – a lack of strong leadership, an absence of a defined vision and goals, and insufficient funding and stakeholder commitment. However, the common thread present in almost all software implementation failures is the explosion of complexity within the design of the software as new features are implemented. The Domain Driven Design website summarizes the point well:

> “Of course many things can put a project off course: bureaucracy, unclear objectives, lack of resources, to name a few, but it is the approach to design that largely determines how complex software can become. When complexity gets out of hand, the software can no longer be understood well enough to be easily changed or extended. By contrast, a good design can make opportunities out of those complex features.”
— www.DomainDrivenDesign.org

The chart below visually depicts the relationship between functionality, complexity, and cost in a failed software project. This type of failure is indicative of the 15% of projects mentioned earlier that were cancelled before deployment.

Failed Software Implementation

<img src="/images/pages/the-agile-difference-1.png" title="Figure 1: Relationship between complexity, functionality, and cost in a failed project" />

The x-axis represents the continually increasing functionality of the software application. The yaxis represents the complexity of both the requirements and design of the software as it was implemented. The green line depicts how, in this project, the cumulative set of requirements became linearly more complex as features were added. The pink line shows how the software implementation of the business requirements became exponentially more complex as features were added. Finally, the shaded light blue area represents the total number of hours dedicated to the project as functionality was added.

The trend is clear – the cost of implementing new features becomes greater as the complexity of the software design increases. Ideally, the complexity of the software solution should closely track the underlying complexity of the problem being solved. In this case, a lack of software engineering knowledge and discipline caused the complexity of the application to spiral out of control. Bad design decisions encouraged more bad decisions and severely limited the availability of good design options as the project progressed. In addition, a larger and larger percentage of the hours spent on the project become absorbed in rework. In an article published in the IEEE Spectrum in 2005, Robert Charette explains the situation:

> “In fact, studies have shown that software specialists spend about 40 to 50 percent of their time on avoidable rework rather than on what they call value-added work, which is basically work that’s done right the first time.<br />
&hellip;<br />
In the simplest terms, an IT project usually fails when the rework exceeds the valueadded work that’s been budgeted for.”

In this case, the allotted budget was sufficient to complete both planned versions of the software. However, you can see visually that because so much of the shaded blue area is above the green line, the budget was expended before the software could ever be deployed. The area between the green and pink lines is often referred to as “technical debt”, or the difference between how complex the software is and how complex it needs to be to fulfill the requirements.

This type of failure often occurs when organizations assume that choosing the consulting company with the lowest hourly rate will result in the lowest implementation cost for the project. The chart disputes this assumption on two grounds. First, the implementation of new features immediately before the cancellation of the project took an order of magnitude more time than it should have based on the marginal complexity introduced by the additional requirement. This disparity more than cancelled out the hourly cost advantage between the chosen team and a more qualified team and would have only grown more acute over time. Second, the entire project was cancelled because the project went so far over budget. This, of course, means the organization will receive little, if any, return on its investment.

A project like this one usually follows a predictable trajectory. Like a brisk hike through the meadows at the foot of Mount Everest, the beginning of the project is usually marked by optimism on the part of all involved. In fact, if you look closely at the chart, the complexity of the software design closely tracked that of the underlying requirements during the first part of the project. This is because the initial requirements and, more importantly, the initial software design were both inherently simple at the beginning. At the beginning of the project, features were released frequently and for the most part without errors.

During the middle phase of the project, however, chinks in the armor begin to become exposed:

- Bugs begin to appear more frequently when new features are added
- The implementation time for new features begins to grow mysteriously
- The team begins to become agitated by requests for new features
- Team morale begins to sag
- Project sponsors still remember the project’s successful beginning and most believe that the current quality issues are normal and will abate as the project draws closer to completion

Towards the end of the project, the wheels begin to fall off. The warning bells that began ringing quietly during the middle phase can no longer be ignored. Non-critical features planned for release are jettisoned. The organization becomes like a gambler who won a big hand to start his night but has since gone deep into debt. How much more money should it invest before deciding to cut its losses and return empty-handed?

Fortunately, this outcome is entirely preventable. The key is the rigorous application of the best practices engendered by agile software development, test-driven development (TDD), domain driven design (DDD), object-oriented analysis &amp; design (OOA&amp;D), and automation. When applied by industry-leading software developers, these practices offer a radically different alternative to the failure that is all too common in custom software development.

## Why Custom Software Projects Exceed Their Budgets

Like failed software projects, projects can be delivered over budget for a number of reasons. An unrealistically small budget, the lack of an iterative development approach, and insufficient status reporting and oversight are all possible causes. However, as is the case with failed software projects, the culprit is most often the unchecked introduction of complexity into the software design. The diagram below is representative of the 51% of software projects that are delivered over-budget or without critical features.

Over-Budget Software Implementation

<img src="/images/pages/the-agile-difference-2.png" title="Figure 2: Relationship between complexity, functionality, and cost in an over-budget project" />

The diagram looks similar to that of a failed software project. The only key difference is the incline of the complexity curve. In this case, the unnecessarily costly addition of new features was tolerable during the development of the first two versions. The project cost over twice as much as expected, but it was released. It has added value, and, hopefully, more value than it cost to implement. However, in addition to the budget overage, the less-than-optimal implementation has resulted in lost opportunity costs which are difficult to measure. Worse yet, the application will most likely need to be rewritten before a fully-functional, third version can be released.

As the statistics indicate, this scenario is much more common than complete failure. Although not a complete loss, it still puts the organization in a difficult position. Those who approved the funding of the first implementation most likely did not do so with the expectation of needing to replace the system so soon.

Now the project sponsors are put in the position of the owner of an old vehicle. How long should they continue spending money on increasingly expensive repairs and enhancements before replacing the system? In addition, if they do replace the system, what guarantee do they have that the next implementation will be a better investment? With software development, an old expression holds true: “If it’s worth doing, it’s worth doing right.”

## How Agile Delivers Software Success

Headspring Software Implementation

<img src="/images/pages/the-agile-difference-3.png" title="Figure 3: Relationship between complexity, functionality, and cost in a Headspring software project" />

The dashed green line in the chart represents a client’s original requirements. The solid green line demonstrates how Headspring Systems can help clients simplify their requirements in two ways.

During implementation, Headspring consultants strive to become experts in the client’s domain. This enables them to partner with clients to develop viable, alternative solutions to problems that will ultimately be less costly to implement, and more importantly, maintain. When applied rigorously throughout a large implementation, this discipline can have a profound effect on the quality of the final product.

The second important way Headspring works with clients to simplify requirement is through the application of the “80/20” rule. The rule states that in many cases 80% of the value of a feature can be delivered for only 20% of the planned cost (and complexity). The corollary, of course, is that the remaining 20% of the value will consume the remaining 80% of the planned cost.

By helping clients recognize these special cases, Headspring Systems can help clients prioritize development work to maximize the value received within a given budget. The remaining 20% of lower-priority functionality can then be made into a separate story and moved to the backlog where it will be addressed once all of the highest-priority stories are implemented. This approach often presents project owners with unexpected opportunities – high-value user stories planned for the second version can often be moved up to the first version. In addition, the software may be released early to a smaller audience of users to increase feedback and realize return on investment sooner.

The biggest difference in the Headspring project diagram versus the others is that complexity increases linearly as new functionality is added, and closely tracks the complexity of the underlying requirements.

You can see visually how much less of the shaded blue area appears above the green line. Instead of rewriting applications after every two or three major releases, a client’s investment in custom software assets can be leveraged indefinitely. Headspring accomplishes this outstanding performance through industry-leading project management and engineering principles.

## Agile Project Management

Agile management keeps complexity from growing exponentially compared to functionality by taking an iterative approach to development, ensuring the involvement of stakeholders, and creating a transparency into design and process in which code is owned collectively and “knowledge silos” cannot materialize. Staples of Agile include:

* Less risk

  * More frequent releases

* Better requirements

  * Decisions made as late as possible when the most is known

* Better communication

  * Team co-location

    * Stakeholders near engineering team

    * Engineering team within a single bullpen

  * Emphasis on face-to-face communication

  * Informative workspace

    * Daily-updated sprint burn-down chart

    * Story board showing all sprint stories and progress against plan

    * Key design artifacts for the sprint such as sequence and class diagrams

  * Daily standup

  * Weekly sprint review

  * Weekly sprint retrospective

    * Helps optimize team performance as the project goes

  * Weekly sprint planning and estimation

* Less wasted documentation effort

## Extreme Programming Engineering Principles

The previous section discussed the many benefits of agile software development. However, to accept Agile as a valid approach, it’s important to understand why the waterfall method has been the predominant choice of software implementation teams for decades. Iterative processes have been known about since at least 1970 when Winston W. Royce introduced what is now known as the Spiral Model. There must be a reason it is so heavily favored.

The central justification for the waterfall method is that changing software is prohibitively timeconsuming and risky, and should therefore be minimized or avoided altogether. By iteratively developing the requirements on paper before implementing any software, the theory holds that each section of code will be written once and will not be subject to frequent changes due to design flaws discovered during implementation.

The waterfall approach sounds logical, but it has one critical flaw. There are always numerous ways to meet an organization’s objectives through custom software. Better feedback will always be generated by the organization as it reviews functioning software than when it reviews hundreds of pages of user interface wireframes, flowcharts, and engineering schematics. In addition, the requirements and design documentation is generated at a time when the implementation team knows the least about the organization and its needs – at the beginning of the project. This means that in practice, implementation teams are either pitted against their project sponsors by refusing to accept valuable feedback, or they are forced to change the software through a series of iterations until sign-off is obtained.

Whether they realize it or not, software teams responsive to client feedback usually begin to abandon original requirements and design documentation as a project progresses and emulate Agile software development, instead. Software teams often look back on original requirements and design documents and laugh when they realize how different they are from the final product. In fact, it is no laughing matter. These teams often spend a fifth or more of their total budget on documentation that becomes unusable before the completion of the first software release.

The advantages of Agile software development are clear, but Agile alone does not address a fundamental question: “How can we ensure that the changes made to existing software are done in a manner that is both low-risk and cost-effective?” The inability of software teams to answer this question explains why so many prefer the waterfall method. If a team can’t reliably change software in a timely manner, it will choose a process like waterfall or the Rational Unified Process that resist change as much as possible. Headspring’s use of Test-Driven Development (TDD), Domain Driven Design (DDD), Object-Oriented Design (OOD), and automation provides a comprehensive answer to this fundamental question. These leading industry-leading best practices provide the engineering agility that a true Agile software development methodology demands.

## Test-Driven Development

### Overview

Test-Driven Development is by far the most important engineering discipline Headspring Systems utilizes to ensure the software it develops can be easily enhanced without introducing defects. The importance of its usage cannot be over-emphasized – it is as important to software engineering as double-entry bookkeeping is to accounting. Yet, amazingly, the overwhelming majority of software development teams do not practice Test-Driven Development. It’s hard to imagine the chaos that would reign in corporate finance if only 10% of accounting firms understood and utilized double-entry bookkeeping. Yet, this level of chaos is exactly what passes for the status quo in software engineering where only 34% of projects succeed.

Test-Driven Development drastically reduces the discovery time of software defects, often preventing them altogether. In the IEEE Spectrum article, Robert Charette discusses the danger of bugs that go undiscovered:

> “The sooner the omission is detected and corrected, the better. It’s kind of like knitting a sweater. If you spot a missed stitch right after you make it, you can simply unravel a bit of yarn and move on. But if you don’t catch the mistake until the end, you may need to unravel the whole sweater just to redo that one stitch.<br/><br/>
If the software coders don’t catch their omission until final system testing—or worse, until after the system has been rolled out—the costs incurred to correct the error will likely be many times greater than if they’d caught the mistake while they were still working on the initial sales process.<br /><br />
And unlike a missed stitch in a sweater, this problem is much harder to pinpoint; the programmers will see only that errors are appearing, and these might have several causes.<br />
&hellip;<br />
Once a piece of software makes it into the field, the cost of fixing an error can be 100 times as high as it would have been during the development stage.<br /><br />
If errors abound, then rework can start to swamp a project, like a dinghy in a storm. What’s worse, [is that] attempts to fix an error often introduce new ones. It’s like you’re bailing out that dinghy, but you’re also creating leaks. If too many errors are produced, the cost and time needed to complete the system become so great that going on doesn’t make sense”

Robert Charette makes several important points. First, the longer a software defect goes undetected, the more costly it becomes. Second, he alludes to how difficult the source of a defect can be to pinpoint. Finally, he describes how introducing new defects while fixing existing defects can initiate a vicious cycle of rework that swamps the project budget and sinks the project. Fortunately, Test-Driven Development effectively addresses all three of these issues. To understand its strengths, it’s important to understand how Test-Driven Development works.

### How it Works

The practice of Test-Driven Development is straightforward. During requirements analysis, large tasks are identified that the software must perform. For example, searching for records based on a number of search parameters, or importing a large data file. Through object-oriented design, these large tasks are divided into numerous sub-tasks or responsibilities. Each responsibility is then assigned to a granular software component called a class.

Before coding the new class, a separate piece of software called a test fixture is created which acts as an executable specification of the class. The test fixture contains tests that define the inputs and the expected outputs and behavior of the class. Only after the test fixture is created and validated is the class implemented to satisfy the specification supplied by the tests in the fixture.

Once created, the new tests are executed as part of a growing suite of automated regression tests immediately before and after each software modification is finalized. If any software fails to satisfy its specifications, it is an indication that a defect has been introduced and the developer will not commit his or her changes to the source control repository.

The execution of the automated test suite immediately after a change is committed as a safeguard to protect against developers who forget to execute the tests before committing. In practice, however, this rarely occurs because the identity of a developer who “breaks the build” is revealed to the implementation team within minutes of the mistake through the use of a separate process called continuous integration.

The graphic below visually depicts the feedback developers receive when they accidentally introduce a defect into their personal copy of the software. This defect must be corrected before the developer can commit his or her changes to the shared source code repository. Figure 5, includes the entire section of source code covered by the failing test. It demonstrates how a failed test allows developers to immediately pinpoint the exact location of a bug.

Execution of Regression Test Suite

<img src="/images/pages/the-agile-difference-4.png" title="Figure 4: Execution of an automated test suite in which one test failed" />

Pinpointing the Defect

{% codeblock lang:c# Figure 5: The failed test pinpoints the source of the defect to a few lines of code %}
public int GetInteger(string columnName)
{
	int value = int.Parse(GetString("columnName"));
	return value;
}
{% endcodeblock %}

### Advantages

#### Identify and Correct Defects Immediately

Before committing their work to the shared version of the source code, developers first implement and test their changes locally on their own workstations. By using Test-Driven Development, developers are informed about the defects they have accidentally created before the bugs are ever committed to the shared version of the code.

#### Enable Developers to Safely Modify Code Written By Any Other Team Member

On teams that don’t use TDD, there is often an unwritten rule that only the original author of a piece of code can modify it. Without a specification to completely define how the software should work, it can be difficult to discern a defect from intended behavior. A test fixture written by the original author forever captures and enforces the intended behavior of the corresponding software. Once under test, the code can be reworked by any team member without fear of introducing defects, even if the original author is no longer part of the team or is, for example, on vacation.

#### Enable Faster Implementation of Stories

Modifying code not written using Test-Driven Development is a lot like rock-climbing without safety equipment. Those who don’t practice TDD assume that it is more time-consuming than traditional development. However, that’s a lot like saying that the use of ropes and karabiners to climb a difficult wall is unnecessarily time-consuming. Without safety equipment, even good climbers will proceed more slowly, planning every move with extreme care and double-checking each hold before proceeding. While it does take time to set up and operate the equipment, climbers can be far more aggressive and move more quickly when their confident their safety equipment eliminates the risk of mistakes.

When modifying code without automated test coverage, developers must perform an exhaustive impact analysis beforehand and extensive manual regression testing afterwards. The presence of automated tests let developers begin coding after performing only minimal research and almost completely eliminates the time spent performing manual regression testing.

#### Pinpoint The Root Cause of Defects Quickly

Test fixtures designed to validate the functionality of a single class contain unit tests. Unlike manual application testing which can easily exercise thousands of lines of code all at once, unit tests are laserfocused, usually testing no more than ten lines of code each. When a unit test fails, it points the developer to the exact location of the defect. Without unit tests, developers are forced to manually wade through hundreds or even thousands of lines of code to find the problem.

#### Prevent the Reintroduction of Defects

One of the most common aspects of a failing software project is the constant introduction of new defects while trying to correct existing ones. Statements like “you fixed the search screen but now the details page won’t load”, become commonplace. In a failing project defects also tend to be corrected and reintroduced many times.

## Domain-Driven Design

DDD is not one of the tenants of Extreme Programming but most XP professionals find that it goes hand and glove with Agile and XP. In Domain-Driven Design, object-oriented programming dominates the code base. All database tables correspond to objects and all objects correspond to stakeholder concepts so there is never the need for the “translation” from ideas to objects to data which balloons complexity in other software undertakings. Domain-Driven Design ensures ubiquitous language.

## Object-Oriented Design

When objects are scripted for Domain-Driven Design there are considerations which will keep code uncluttered and malleable. Good software designs all share three characteristics. They are:

* Composed of small, loosely coupled classes
  * IoC
  * Interface-based Design
  * Testable classes
* Well organized so that each class has its own responsibility
  * Single Responsibility Principle – Patterns
  * Make extensive use of reuse so that a no two class repeat the same responsibility
* Make liberal use of open-source software libraries to reduce the size of the code base
* OR Mapping

## Automation

To fully implement a new user story, several steps must be completed. First, it must be coded by a developer on his or her workstation. Second, the new code should be compiled and unittested when it is committed to the team’s shared source code repository. Third, it must be fully integration-tested and certified by the quality assurance team. Finally, the software must be deployed to the production environment where it can be accessed by the target audience of end users.

Without proper automation, each step in the process requires the completion of timeconsuming, repetitive tasks that waste time and distract the engineering team from its core mission – the implementation of software that increases the effectiveness and efficiency of the client organization. Ironically, most software engineering teams fail to leverage the technology available to them to automate these steps and increase their own efficiency. Headspring Systems automates the repetitive tasks of each step in the process using: automatic code generation and refactoring, continuous integration, automated integration testing, and automated deployment.

### Automatic Code Generation and Refactoring

While most .NET teams code using Microsoft’s Visual Studio, few use advanced code generation addins. Headspring Systems leverages one such add-in, called Resharper, to dramatically reduce the physical typing time required to generate new code and perform basic refactoring operations such as class and method renaming.
Headspring also uses tools to generate all of the Database Definition Language (DDL) code necessary to modify the structure of an application’s database over time. For example, Red-Gate SQL Compare generates sophisticated SQL Server DDL automatically that returns the database to its original state if any errors are encountered during execution.

### Continuous Integration

Continuous integration refers to a series of tasks that are performed each time a change is committed to the production code base. First, the source code is compiled into executable binary files. This step will fail if there are any syntactic errors in the source code. Next, the code is unit-tested using the test fixtures created via Test-Driven Development. This step ensures there are no logical errors in the software.

Together, these quality assurance steps can be compared to document editing. The first step, compilation, is analogous to the execution of the spelling and grammar checkers in Microsoft Word. The next step, unit-testing, is a more in-depth examination of the code which is analogous to the proof-reading of a document. However, unlike document-editing, this step can be automated using the specifications present in the suite of automated unit tests.After the source code is compiled and unit-tested, it can optionally be deployed to a demonstration environment where it may be reviewed by project stakeholders. This gives stakeholders unprecedented access to the most recent revision of the software.

Finally, vital statistics about the health of the code base are published to a website where it can be reviewed by the team. Using this information, the team’s lead architect can detect sections of code that are unnecessarily complex or are not properly validated by unit tests and take corrective action.

### Automated Integration Testing

Headspring Systems employs two different types of integration testing: Functional Integration Testing (FIT) and User Interface Testing.

The best way to understand FIT is to look at a typical FIT test:

FIT Test

<img src="/images/pages/the-agile-difference-4.png" title="Figure 6: Typical FIT Test with Results" />

The requirements document above defines how to calculate employee wages. More importantly, though, through the use of FIT, this requirements document has actually been executed against the wage calculation software. Notice the last column of the table – the first two results are green indicating the software correctly calculated the employee’s wages. However, the third result indicates there is a bug in the software per the requirements document. The employee should be paid $1360, but instead would only have been paid $1040 if the software defect hadn’t been identified by the failed FIT test.

Like unit tests, FIT tests are invaluable assets that Headspring Systems delivers with the software it implements. Once written, an entire suite of FIT tests can be run as a batch on an hourly or daily basis to ensure user story implementations always meet their documented specifications.

User interface testing is a second type of integration testing that focuses on validating the software application from an end-user’s perspective. When user interface tests are executed, it appears as though an invisible robot has taken over the tester’s workstation. The test opens a new web browser and navigates through the web application to ensure the expected output is displayed on each page. Although it follows the same steps a human tester would, the automated test executes many times faster. In addition, like FIT tests, a suite of user interface tests can be run automatically as often as necessary to ensure all of the pages within the web application continue to execute properly as new stories are implemented in the software.

A manually executed test of software only proves the application worked properly at the time the test was performed. When a single change is made to the software, the test result can no longer be trusted. On the other hand, the time invested in creating an automated unit or integration test continues to add value for as long as the software is in use.

### Automated Deployment

There are many audiences of an application as it is developed. Developers implement user stories, testers validate the story implementations satisfy requirements, stakeholders give final sign-off that the software meets expectations, and trainers teach people to use the software through demonstrations and hands-on lessons. These activities cannot be performed against the production copy of the software because it is used by the most important audience, the end users for whom the software was built.

To optimize the effectiveness of these development activities, it is critical that each activity be performed against a different copy of the application. Consider what would happen if a developer made a change to the software during a trainer’s class or the execution of an automated test suite? What would happen if a tester deleted data for testing purposes while a stakeholder was reviewing the information? The key is to have each developer and tester work with a personal copy of the software. Other roles such as stakeholders and trainers can often share copies of the software.

With so many deployed copies of the software, it is important to automate the process of copying the software to each location. The deployment process involves copying the software to the correct computer, configuring the software, and upgrading the database to account for any structural changes made during development. Headspring Systems automates each step in the process so that it can be performed seamlessly. Most importantly, the process enables production deployments to go smoothly preventing unnecessary down-time for the system’s end users.

## Conclusion

This document has illustrated both the inherent flaws with traditional software development and the means that a team may undertake to clear the hurdles. The pitfalls may be avoided by undertaking Agile development, Extreme Programming engineering practices, and Domain-Driven Design. The Agile Difference is one between flying blind and successful projects.
