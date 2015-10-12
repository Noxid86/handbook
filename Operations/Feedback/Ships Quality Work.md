# Feedback: Ships Quality Work

[Back to the Feedback Template](https://github.com/devmynd/handbook/blob/master/Operations/Feedback/Feedback%20Template.md)

At DevMynd, we want to ship quality code, designs, and products that we can be proud of. That's an easy thing to say, but it's actually quite difficult to achieve all the time on a real-world project, where there are inevitably competing priorities.

Some developers have a well-developed “gut feel” that tells them when code is high quality and when it's not. Despite that, an actual definition of “quality code” is hard to pin down. Here are some questions to consider when you're trying to decide whether the code you're working on fits:

* Would you want to come back and maintain this code in a month? A year? Five years?
* Would you want other developers to look through this code?
* How confident are you that 1) changes in one area won't silently break something somewhere else and 2) it works the way it should under all circumstances?

These are fairly abstract questions, so we've put together some tactics our developers can do that generally lead our code in the right direction.

**1. We consider solutions and consequences before diving into coding.**
**2. We do “just enough” planning.**

These tactics are two sides of a coin. We want to make sure we think through technical decisions before we leap in and write a bunch of code, so that we don't end up with, e.g., the wrong data store or the wrong framework. However, we don't want to over-architect or “gold-plate” our code either. Remember: you ain't gonna need it (YAGNI). When you're about to add another abstraction, ask yourself if it makes the code more clear, or less clear.

**3. We write clear code that communicates intent.**

Try to make each piece of code reveal what it does, without requiring other context. Apply the “inebriation test”: could someone who gets paged on a Friday night and has had a beer come in, look at this code, understand it, and change it?

**4. We write clear specs that test the right things.**

Our tests are often the only documentation for our code. They should tell a developer new to the project what the code does, without getting into the details of how it is done. Individual tests are small. We test our code -- not framework code -- and we make sure that both the happy paths and the sad paths are covered at the appropriate level of detail.

**5. We aim to test-drive all our code.**
**6. We aim for all code to be reviewed, preferably in real-time by a pair.**

These two tactics ensure that code used by customers does what they expect. In general, our goal is to test-drive and pair on all code. We want developers to seek out these practices, and the leads' job is largely to make this possible.

However, soloing and spiking are both unavoidable, so our standards are different for production code (executed by an end-user) and non-production code (only executed by developers). All production code should be paired on and test-driven; when that's not possible, seek a review before pushing it to master. And every project always has some non-production code tasks (backfilling tests, updating CI build scripts, etc.) that make good soloing material.

**7. We give careful consideration to requested divergences from our quality standards.**

As mentioned above, real-world projects have competing priorities.  Writing high-quality code takes more time in the short term than writing low-quality code, which means the priority we place on it will sometimes be at odds with, e.g., an investor demo, an app store deadline, or a checklist of features the customer came in with.

Our style of development presents us with this dilemma:

<img src="https://raw.githubusercontent.com/devmynd/handbook/master/Operations/Feedback/quality-scope-deadline.png" />

If code quality and scope are fixed, then the deadline has to be negotiable. If code quality and deadline are fixed, then the scope has to be negotiable. And, of course, if scope and deadline are both fixed, then code quality has to be negotiable.

DevMynd's focus on writing high-quality code is one of our differentiating factors, both as an employer and as a consulting company. That's why we can't take projects that have both a fixed scope and a fixed deadline; at least one of those two must be able to move, so we can maintain code quality.

As a result, we encourage the customer to shift their thinking on scope and/or deadlines. These can be adjusted by moving stories around and deciding what is necessary and when. Code quality can only be adjusted by removing or avoiding tests, bypassing refactoring opportunities, skipping automation steps, and so on. None of those things make DevMynd look professional, or create long-lasting benefit for the customer.  These sorts of compromises also just make us feel bad as developers, because we can't be proud of that code.

All DevMynders should feel empowered to push back on schedule and scope pressure when it's infringing on code quality.

That said, we aren't dogmatic -- we do sometimes compromise on code quality, when it is really warranted. But when we do, it's a conscious decision rather than the ‘natural' result of schedule pressure, and we make sure the customer really understands the tradeoff we're making on their behalf.

And we definitely bring it up at the next retro.

[Back to the Feedback Template](https://github.com/devmynd/handbook/blob/master/Operations/Feedback/Feedback%20Template.md)
