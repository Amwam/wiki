# How to Code Review

- Not for finding bugs
- Making sure you understand
- Is it going to be easy to maintain
- Could I manage if I was the only one on support and had to fix something with it.
- Can we split this up into smaller pieces
- Learning something new about the system
- Don't pick on style preferences (tabs vs spaces), we have prettier and black for that.
- Ask questions
- Common issues
  - Performance problems
  - issues i've seen before
  - Are the permission checks setup/correct

- how do you find time to do code reviews?
  - CR should be a part of your "work", make time for it, its just as important as writing code and planning new features

- What are the red flags you notice in a code review?
  - size
    - the more mental capacity it takes to review, the more likely i am to ask for it to be split
    - lots of the same repeated changes, like a conditional inserted into multiple files all over the place

Its a shared codebase, were all responsible for it, and its maintenance. 