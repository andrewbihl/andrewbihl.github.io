---
title: My highlighting system for reading technical content
date: 2020-05-25T11:00:00Z
description: How I understand and retain information from expository writing
location: San Diego, CA
showLocation: false
tags: [learning, productivity]
article: true
thumbnail: ./highlights_ddai.png
---

> And science is, to quote your words, nothing but the 'determination to establish differences.' Its essence couldn't be defined more accurately. For us, the men of science, nothing is as important as the establishment of differences; science is the art of differentiation.

– Hermann Hesse, Narcissus and Goldmund

## Summary

In my experience, much of learning technical information comes down to drawing categories and relationships. I've found that by highlighting statements as I read by their purpose, I can more quickly understand the information being presented. It also helps me stay focused and see which statements I didn't comprehend on first pass. I assign statements one of five functions:
- points
- limitation
- evidence
- value
- background

These functions align with a more general view of learning in which the functions contribute to a step in the learning process.

## Motivation: the learning process

I believe the system works because it helps me to navigate a path to comprehension by making it clear how each statement contributes to the path.

For me, understanding something often follows a common sequence of steps:
- Categorization
- Relation
- Nuance
- Application

### 1. Categorization

First is to put things into buckets. I learn names and definitions (though I likely won't fully grasp the definitions at this stage), and put some examples into one bucket or another. I see how the subject relates to things I already know or have heard of.

- Names: *There are "compiled" languages and there are "interpreted" languages.*
- Examples: *Python is an interpreted language.*
- Definitions: *In a compiled language, the target machine directly translates the program. In an interpreted language, the source code is not directly translated by the target machine. Instead, a different program, aka the interpreter, reads and executes the code.* <sup>1</sup>


### 2. Relation: understanding the purpose of the categories

Categories are conceived for a reason. The next step is to learn the distinctions between categories and the reason for their designation. This usually means accepting broad statements for the sake of retaining the general idea.

- Details of differences: *An interpreted language is translated by an "interpreter", whereas a compiled language is translated by a "compiler".*
- Value comparison: 
    - *Compiled languages run faster.*
    - *Interpreted languages are simpler.*

### 3. Nuance: breaking down the categories

Categories are almost always imperfect<sup>2</sup>. This doesn't diminish their usefulness, but real understanding means seeing the limitations of categories. This step is where things may be broken down further into subcategories, or perhaps be understood as a continuous axis instead of a discrete category.

- Non-fitting examples: *Java is a sort of hybrid. It's compiled to an intermediate representation which can then be interpreted by the Java Virtual Machine.*
- Limitations: *In theory, any language could be interpreted or compiled. The distinction is in how it is executed on the machine.*

### 4. Application: using what you learned

Depending on the situation, this step and the last might go hand-in-hand. It depends what you are trying to do. Often, the more involved the goal you have, the more of step 3 you'll need to do. In the example of learning about types of programming languages, you could have a number of different goals. Some examples could be:

- Decide on a programming language to use.
    - This probably doesn't require a huge amount of nuance, so you might not dive too deep into step 3.
- Write a compiler
    - This application lends itself to helping you learn #3. It's likely worth diving into the "Application" step early.
- Write a textbook on programming languages
    - This is going to require a lot of nuance, so application will probably not begin until you've done a lot of step 3.



## The system


![Excerpt with highlights from Designing Data Intensive Applications](highlights_ddai.png)

My annotation system highlights statements belonging to one of a limited set of categories in order to make clear the structure of what is being said. For expository writing, those categories are:
- points
- limitations
- evidence
- value
- background

### Point: a statement which is part of the main idea set, including explaining the meaning of an earlier point

A point is a statement which answers the question “what is the author trying to say?” It requires elaboration. It may require convincing the reader of its accuracy; it may require explaining its significance; it may have supporting examples, which can serve either of the two purposes just mentioned.

To clarify what makes a point, consider this scenario: you are writing to an audience which has all of the same background knowledge you do, already cares about the subject and knows its importance, and believes you to have absolute autority on the subject. Any statement you make will be immediately understood and believed, and its usefulness immediately grasped. 

 In this circumstance, you provide no background information, no evidence, no justification of the statements or their value—you simply state the main thread of idea so that you wish to portray. You simply provide a list of points.

### Point limitation: acknowledging challenges

This is similar to point. It’s like explaining an earlier point (which would still be categorized as a point) except that it refines or restricts the idea. It admits failures, exceptions, limitations, and counterpoints. It can also describe unanswered questions and areas of ongoing inquiry. Limitations provide clarity on the bounds of an idea.

In technical writing, I like to use this category for descriptions of drawbacks of a given approach or technology. 

### Point evidence: convincing the reader of the truth of a point

Evidence is a statement, often in the form of an example, which serves the purpose of convincing the reader that earlier or soon-to-be-revealed ideas are correct.

### Value: telling the reader why the point is important or relevant

This is a statement, often in the form of an example, which serves the function of convincing the reader that the point is relevant and useful information. This may be historical context or instances where the point was used by others. Often it is directly telling the user how to apply the information.


### Background: necessary prior knowledge

This is necessary prior knowledge which is provided so that other statements will make sense but which is not part of the above categories. In many books, this may take the form of a reminder of content found earlier in the book, which in its own chapter would be considered points. Later on, however, the author will assume the reader accepts his ideas in order to permit him to build on top of them. 

I find that it is helpful to use this category for definitions even if the term has just been introduced for the first time. While it may not be knowledge that the author expects the reader to already have, it is not up for debate or requiring justification. That is, the definition is not a point—if the author could be sure the reader already had this information, it could be excluded from the writing.


## Applying the system

By following this system, I believe it is substantially easier to progress through techincal reading, especially dense material. You should find it gets easier over time to see how the statement serves the author's overall purpose and quickly annotate it. 

Finally, some details on how to implement this in your own reading:
- You can annotate by highlighting, or by writing a letter near the statements in the margins–whatever works for you.
- A sentence can have more than one statement.
- Not all statements should be highlighted. Highlight those that are important to you, and if a block of statements with the same purpose are together just highlight a summarizing point or the first one.
- Adjust the details of how you categorize as needed.
- Pay close attention to those statements that you're not sure *how* to categorize. You may learn by figuring it out.
- Let me know if you get use out of this, I'd love to hear about it.


----
1. https://www.freecodecamp.org/news/compiled-versus-interpreted-languages/
2. The physical world is infinitely complex, so categories will fail to capture that complexity. However, categories can be perfect when they describe constructed worlds. Mathematics, for example, can have perfect categorizations of mathematical concepts because they are so defined. Simulations, such as computer programs or board games, have a limited number of states so they can also have perfect categories.
