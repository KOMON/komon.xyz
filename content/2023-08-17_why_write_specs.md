+++
title = "Why Write Specs?"
date = "2023-08-17"

[taxonomies]
tags = [ "shorts" ]
+++

"Why waste time writing a spec?"

I hear this a lot. It's usually right along other arguments like:

- "Let's just get this thing built, writing a bunch of docs before we can build anything will slow us down"
- "Doing a Big Design Up Front isn't Agile"
- "If you want to know what the API does, you can just read the code or the tests!"
- "This API is for internal-use only, we don't need to write docs for it"

In response to all of these I have one argument that IMNSHO justifies the opportunity cost of writing specifications:

"Code only says what it does, not what it _should_ do"

Having a readable specification, in whatever form you choose, allows you to:

- Communicate directly and declaratively what the behavior of the system ought to be, reducing guesswork and your bus factor
- Evaluate if the system is behaving correctly whether you've never seen the code or if it's been months since you've last looked at it
- Building to a spec allows more work to be done in parallel as you're not blocked by pieces that haven't been implemented yet

You needn't spend months writing the perfect, exhaustive spec either; good specs are living documents that grow and evolve alongside the system they describe.

Plus, specifications allow ancillary benefits:

- API spec tools like OpenAPI/Swagger can be used to generate pretty docs and client SDKs
- Executable specification languages such as Alloy or TLA+ can enumerate the constraints and properties of the system and validate their correctness before you do the work to implement them
- Even just writing out some type definitions and interfaces that form the system boundaries in the implementation language of your choice can form the first unit of code review for a new change and allow for input and feedback from the team

Specification is most of what a software engineer does in the first place; don't let your hard work go uncaptured and evaporate into the unknown when you move onto a task.

Write your specs and reap the benefits!
