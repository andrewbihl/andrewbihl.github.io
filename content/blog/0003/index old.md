---
title: On documentation and how companies should think about sharing knowledge
date: 2020-05-26T18:00:00Z
description: A company Google drive is not enough
location: San Diego, CA
showLocation: false
tags: [software engineering]
article: true
# thumbnail: ./highlights_ddai.png
---


I write a lot of notes when I work. At my job (as a software engineer) this is a relatively known fact, to the point that I've had coworkers message me out of the blue to ask if I have any charts or notes that might help them get acquainted with a particular part of the system. This happened today, and while I appreciate the recognition I think it's a symptom of a general problem.


## The problem

I've never worked at a place that had figured out quite what to do about written knowledge. Some were better than others, but from my perspective none had a solid system for sharing knowledge within the company. Most had a good setup for one or two particular types of writing, but other categories were neglected.

I don't think I'm just a pessimistic jerk. Rather, I think managing written information is a hard challenge worth working on. Furthermore, based on forum comments, interactions with coworkers, and online articles, I think I'm more of an optimist than most when it comes to improving the situation. Common refrains from engineers are:

- documentation is never correct
- documentation is never up-to-date
- documentation is never read
- documentation is a pain to write
- just read the source code <sup>1</sup>

The conclusion usually is that maintaining written information is either impossible to do well or not worth the effort. I don't agree, and while I can't prescribe a comprehensive solution to the issue, I have some ideas on how to frame the issue to make it more approachable.


## Clarifying the problem

In my experience, teams have one or two avenues for writing that are used consistently. Unfortunately, when this is the case then all types of writing tend to get put into the existing avenues. For example, comments in source code are not a good place to write product design goals, and Slack is not the best place to do substantial planning infrastructure planning. But if you have something to write and only a couple places you know to put them, it's likely to be stored somewhere inappropriate or lost altogether.

I think it is extremely difficult to figure out how to manage one category of writing without recognizing its scope and how it differs from other writing. If everything gets dumped into one place, it can make it hard to retrieve the information needed. Consequently, to maintain organization I think the expectations have to be clear around what a particular avenue is for.

If we take for granted that there is value in sharing and preserving information within a company, then the shortcomings can be described as issues of execution.

Concretely, the issues at hand are:

- How do you get people to write?
- How do get the information to be accurate?
- How do you keep the information alive and up-to-date?
- How do you surface the information to those who need it?



My claim is this: **the type of writing determines the answers to these questions, and your tools and processes should be appropriate for each.** To start to think about how you should manage your writing, you should first answer **four questions about purpose**:

- What is being written?
- When should it be written?
- When should it be read?
- When should it be updated?

For every one of these purposes, you must then answer: **How is that accomplished?**

## A simple example

Take an example: you have a section of code that is sufficiently complicated to require explanation. Where should this explanation be written? 

This is an easy one. You want this information:
- to explain the purpose and/or logic of the code
- written when the code is written
- read by other people who need to understand that code
- updated when the code changes meaningfully

Naturally, most would say this belongs as a comment in the source code. It's a convenient place to write it when you're working on the code, and you're likely to see it when you need it. All of your questions can be mostly solved by putting it in source code and by encouraging teammates to review doc comments as well as code when they review merge requests.

## More complicated cases

Other cases are not so easy. Imagine asking your team to write a detailed specification of your system, or a wiki for constantly-changing internal tools. Consider a one-off question is posed on Slack which turns out to be asked often by new engineers.

When considering these cases, answering how to accomplish those four questions will lead to more detailed questions like:
- How can I encourage my team to write?
- How can I surface the information to those who are searching for it?
- How can I surface the information to those who need it but don't know it?
- How can I make sure it gets updated when things (code, tools, internal processes) change?

I think the right combination of policy, culture, and software tools can solve these problems for any one particular type of writing, but one solution does not fit all. If you communicate everything in Slack, you're not going to have long-form documents describing large systems. If you decide Confluence is your sole information repository, Q&A type information is not going to be written and kept up-to-date.

### Stackoverflow

Consider Stackoverflow as a successful case of knowledge-sharing. How does it solve for its purposes?

- *What is being written?*
    - Goal: Answers explaining things relevant to the topic/tag.
    - Solution: Have a large potential pool of contributors, and a voting system to gauge quality.
- *When should it be written?*
    - Goal: After someone explicitly poses a question, then its answer should be written.
    - Solution: Users can see questions needing answers in topics they know.
- *When should it be read?*
    - Goal: When someone needs the answer.
    - Solution: Have results indexed by Google, and notify the original asker of answers.
- *When should it be updated?*
    - Goal: When the answer changes and the current information no longer solves people's problem.
    - Solution: 
        - Allow the answer to be updated
        - Allow new answers to be added
        - Allow the post to be linked to other posts
        - Other features of the product help with this as well


A lot more could be examined about Stackoverflow, but the point is to see the link between the particular type of information and the tool that solves for its purposes. Stackoverflow includes a lot of features which reward those who answer and make it clear to them that their work is appreciated. This feedback system exists because Stackoverflow understands it is not sufficient to determine what you want written–you have to figure out how to actually get people to do it. This is the kind of challenge you rarely see solved by companies in relation to their internal documentation.

## Approaching the problem

Based on all this, the process of improving the situation of written knowledge sharing at a company would look something like this:

1. Identify some type of information that is worth sharing
2. Answer the four questions describing the purpose of the information sharing
3. Come up with solutions to accomplish those goals
4. Implement and iterate as needed

This does leave out a critical challenge though, which is that it must be clear which information goes where. When establishing an avenue for writing and viewing, make it clear what the category is for. If you do your planning in a Confluence folder, don't have people writing FAQs about the existing product in the same place. If you have a Dropbox Paper directory of onboarding documents, that's not the appropriate place for writing explanations of complicated implementation details of your software. 

I stress that it is critical to be intentional about the organization, because if you end up with everything going into one place, it makes everything hard to find. And if the writing can't be found when it's needed, it's as good as gone.

----

1. I could write an entire article on this point, but let's just say that *any* real-world application is going to entail things that cannot be easily traced through source code, not to mention if you have a ["microservice architecture"](https://www.youtube.com/watch?v=y8OnoxKotPQ) crossing the network at every turn. 
