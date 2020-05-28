---
title: How I think about documentation and knowledge sharing
date: 2020-05-26T18:00:00Z
description: I'm tired of digging around Slack
location: Waynesboro, VA
showLocation: false
tags: [software engineering]
article: true
---


I write a lot of notes when I work. This is a known fact at my software engineering job to the extent that I've had coworkers message me out of the blue to ask if I have any charts or notes that might help them get acquainted with a particular part of the system. This happened today, and while I appreciate the recognition I think it's a symptom of a general problem.


## Most fall short

I've never worked at a place that had figured out quite what to do about written knowledge. Some were better than others, but from my perspective none had a solid system for sharing knowledge within the company. Most had a good setup for one or two particular types of writing, but other categories were neglected.

I don't think I'm just a pessimistic jerk. Rather, I think managing written information is a hard challenge worth working on. Furthermore, based on forum comments, interactions with coworkers, and online articles, I think I'm more of an optimist than most when it comes to improving the situation. Common refrains I see from engineers are:

- documentation is never correct
- documentation is never up-to-date
- documentation is never read
- documentation is a pain to write
- just read the source code <sup>1</sup>

The conclusion usually is that maintaining written information is either impossible to do well or not worth the effort<sup>2</sup>. I don't agree. 

I can't prescribe solutions. Any solution will depend on the particular case and on the team. But I do think that this problem can be improved by choosing appropriate practices and tooling for the situation at hand, and I think it's worth dedicating the effort to understand how to go about solving this.

I have some ideas on how to frame the problem to make it more approachable.


## Defining the problem

If we take for granted that there is value in sharing and preserving information within a company, then the problem can be viewed as one of execution.

I think the core challenges are:

1. How do you get people to write?
2. How do you ensure the information is accurate?
3. How do you keep the information alive and up to date?
4. How do you surface the information to those who need it?

**These are not questions with general answers.** Any answers to these questions depend on the type of information being shared.

To make this concrete, consider question \#4: 

> How do you surface the information to those who need it?

How might different people answer this if asked to recommend a solution?
- Customer support might propose that a good FAQ will surface information to people when they ask common questions.
- A newly-hired engineer may recommend creating an onboarding tutorial for engineers to get them up to speed with tooling.
- A product manager could ask that everyone add links to planning documents in Gantt charts to surface context to provide context there.

The problem here is not bad ideas. The point is that these solutions only apply to a particular type of information and not at all to the other cases.

## Defining the writing

In order to start to come up with solutions to the four core challenges I've listed, we have to answer analagous questions about the case we are solving for. I would like to see conversations about documentation avoid jumping right into proposals and start first with a clear answer to these questions:

- What information is being written? <sup>3</sup>
- When should it be written?
- When should it be updated?
- When should it be read?

Consider one a particularly simple case: you have a section of code that is sufficiently complicated to require explanation for other engineers to more easily understand it, so we want to provide that additional help to other engineers. So where should this information be written, by whom, and when? How do we accomplish that?

Rather than just jumping on a solution, let's answer the questions to define what we're talking about:

- **What information is being written?**
	- An explanation in english describing the way a function or block of code works and why.
- **When should it be written?**
	- Ideally we'd like this to be written when the code is written.
- **When should it be updated?**
	- When the logic of the code changes significantly.
- **When should it be read?**
	- When someone needs to understand the code.


Now we are ready to try to solve the core issues.

## Putting it together

If we've clarified the nature of what information we need to preserve and share, we should find it easier to justify or reject ideas. For example, we always have to choose a place for things to be written and stored. In this case, we could brainstorm the following options:

- The code author posts in the team Slack channel a message explaining the code
- The author writes a document and uploads to a team OneNote notebook
- The author leaves a comment in the source code at the top of the function 

Given the nature of the writing, I would confidently say the last option makes the most sense. If the logic is in one file, why not update it alongside that code? People who need to see the comment are likely to see it **when** they need it, **even if they don't know it exists.** It's little additional effort for the author as well, because it fits well into their workflow. Furthermore, if we align on using doc comments for this type of knowledge, than when reviewing merge requests we can ask for them to be added or updated as needed.

It's possible many would choose this solution without having to think about it. I believe, however, that by breaking down the writing and the reasons for a solution we can learn how to take on harder cases.

## Expanding to harder cases

There are plenty of types of writing which are not so easily solved for, and I'd wager that everyone can identify some type of writing for which there is no clear solution in place at all on their team. As a writer, it is frustrating to feel something is worth writing but know if there is anywhere to put it that people will see it. Usually nothing gets written in that case.

Here are some more diverse examples of useful writing:

- An onboarding doc explaining internal tooling which changes regularly
- Document(s) describing planned engineering work, containing discussion of alternatives and justification of the chosen solution
- A graph showing the architecture of an application backend
- A conceptual document describing how a service functions at a high level
- A step-by-step document describing how to deploy updates
- A guide with pointers on how to debug in different areas of the system
- The answer to a short question which is asked somewhat often
- Notes from a retrospective meeting about team practices and culture
- A list of tasks an engineer is currently working on

For each of these, different questions are more challenging than others. But all of them require solving the same basic issues:

1. How do you get people to write?
2. How do you ensure the information is accurate?
3. How do you keep the information alive and up to date?
4. How do you surface the information to those who need it?


### Stackoverflow

As a thought experiment, consider Stackoverflow as an example of something that works very well. How does Stackoverflow get people to contribute? How does it ensure there are quality answers? How is information kept up to date? Can people find the information they are looking for? Stackoverflow has a lot of features and details which work in different ways to solve these, but ultimately it follows the pattern I am recommending. By scoping out the nature of information you are going to solve for, you can form processes and tooling around that case.

Of course I am not recommending teams drop everything they are doing to build a solution like Stackoverflow for all of their problems. I am only suggesting that if you understand why Stackoverflow works for its content, you can evaluate solutions for other types of content.

## The most critical step

Finally, one of my biggest gripes. I'm going to vent a bit here.

My perspective is not that teams must have a solution in place for every type of information–that would be a ridiculous expectation to set. However, I think we are all shooting ourselves in the foot by neglecting to acknowledge and clarify what we do solve. For any given solution in place, if we don't specify the bounds of what it's for then it will get used for other things. Members of the team aren't aligned on what goes where and everything becomes a mess. 

Things get saved in the wrong place, or there is no place for them and they get lost. Or, most commonly, they don't get written in the first place. But worst of all, **things that are in the right place get buried**. A Dropbox account, a slack channel, even a full-fledged search engine will become useless for information retrieval if too much is put in there that isn't what you want. If you find a folder called "Q2 planning" and it's filled with thousands of unrelated documents, it may as well be empty.

So my first step would be this: before seeking out what new types of writing we'd like to handle, let's make sure we are organizing the writing we have. If there is something the team does well, put walls around it so that it doesn't get buried. Make the rules clear. Write a README telling everyone what goes in there and what does not. 

If the writing people produce to share knowledge is lost to poor organization, they're not going to keep writing.

----

1. I could write an entire article on this point, but let's just say that *any* real-world application is going to entail things that cannot be easily traced through source code, not to mention if you have a ["microservice architecture"](https://www.youtube.com/watch?v=y8OnoxKotPQ) crossing the network at every turn. 

2. Any effort dedicated is a tradeoff, so admittedly there must be some cases when a solution is worth the effort. From my experience, however, there are lower-hanging fruits to be grabbed.
3. Consider not just the subject itself but also the purpose of the writing. An example is to classify as "tutorial", "how-to", "explanation", and "reference" as seen here: https://documentation.divio.com  