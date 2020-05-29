---
title: I'm not sure how to read code
date: 2020-05-28T22:00:00Z
location: Waynesboro, VA
showLocation: false
tags: [software engineering]
article: false
thumbnail: marlborough-maze.jpg
---

![https://www.blenheimpalace.com/visitus/what-to-do/marlborough-maze.html](marlborough-maze.jpg)

Here's the scenario: I'm working on a feature involving a service I have literally never touched before and I don't really know what the service does. I only know to look there because someone more knowledgable than me mentioned it in the JIRA ticket.

I don't think I've heard much discussion about how to read code. Like many practical matters of programming, it didn't come up in college classes. I can't recall seeing it in the types of book that would have it like *The Pragmatic Programmer*. Maybe the topic has just gone under my radar. 

It seems worth discussing. People talk about strategies for reading prose, and that's comparatively easy. Unlike code, you can always fall back on the basic idea that you start at the beginning and go forward; any strategy beyond that is just bonus for your speed or focus or comprehension. Reading code isn't really like that. It's not always apparent where to start, there isn't a clear "end", and there are no sure bets on how its organized.

When being thrown into an entirely new code base, I can't say I've often felt successful without getting some help first. Without any documentation or explanation at all I waste a lot of time, especially if it's a backend component with no user interface  (as opposed to CLIs and application frontends). On the other hand, if I do have the opportunity to talk to someone who knows the code base then I have a pretty good idea of how I like things explained to me.

First, give me the purpose. Tell me what this thing is trying to do but exclude the "how".

Tell me where the interfaces are. This doesn't mean "user interfaces", just interfaces–connections to the outside world. Ultimately, things will roughly boil down to:
- API calls coming in
- API calls going out
- databases being read from and/or updated
- messages queues providing/receiving messages
- files being read from or updated

It's like a function–it can have inputs, outputs, or [side effects](https://en.wikipedia.org/wiki/Side_effect_(computer_science)).


List any special concepts I'm gonna need that I might be missing. A fancy algorithm, some distributed consensus logic, anything specialized–if it's in a Wikipedia article send me that, because I won't learn it on the spot when I encounter it in code.

Finally, warn me where the shitty parts are. If I find code that is counter-intuitive it will catch my attention, because if it's counter-intuitive then it is probably interesting–unless it's shitty. There's probably a good reason or a good story for how it got that way, I understand. I'm not looking to judge. I just don't want to waste my time because I got stuck on something less important than it seemed.

Typically these are the things I like to have explained *and nothing more*. I think of it like going into a labyrinth: I'm not going to remember turn-by-turn directions so just point me to the entrance, give me any tools I'll need, and tell me how to spot trapdoors.