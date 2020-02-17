# The DevOps Handbook: How to create world-class agility, reiability, & security in technology organizations

## Author: Gene Kim, Jez Humble, Patrick Debois, & John WIllis


## Part 1: The Three Ways

### Ch 1: Agile, Continuous Delivery, and the Three Ways
-This is a high-level overview section of the book.
-pg4: Lean principles focus on how to create value for the customer through systems thinking by creating constancy of purpose, embracing scientific things, creating flow and _pull_, assuring quality at the source, leading with humility, and respecting every individual

### Ch 2: The First Way: Principles of Flow
-Value Stream Mapping: 
    * user stories to valued product and lead time associated to those features/projects
    * what are bottle necks? 
        * PRs sitting in review - people don't have the context to review these clearly
        * will give blanket approvals on things
-Reducing Batch Sizes:
    - make sure that we're doing small incremental changes in PRs
    - we can find errors a lot easier
    -smaller tickets in smaller chunks of work
    -draft PRs for good progress made

### Ch 3: The Second Way: Principles of Feedback
-Feedback loops:
    * go to the stakeholders with the wire frames and grab feedback before you start working on something you created

### Ch 4: The Third Way: The Principles of Continual Learning and Experimentation
-Swarming: don't do new work
-Enabling organizational learning: 

1. The Pathological - info is hidden, new ideas are crushed
2. vs. Bureaucratic - responsibilities are compartmented, new ideas can create problems
3. vs Generative organizations - responsibilies are shared, failure creates inquiry

-What is the best one? Is there a best one?
    * how would a company move from one of the first two categories to generative? 
    * how do you bridge teams and reward them for that? 
    * Not throw blame on failures but instead accept them and take them as learning/sharing knowledge?
        * does that come from a team-by-team basis? or does it have to come from the top?


## Part 2: Where To Start

### Ch 5: Which Value Stream To Work With
-greenfield vs brownfield projects - you can develop the devops system with either, though there is a myth it needs to be a new project (greenfield)
-Nordstrom example where they were able to dedicate a team to prioritize fixing certain things
-don't just throw more people at the problem - try to fix how it's working

### Ch 6: Understanding the Work in Our Value Stream
-pg69: 20% time should be used to pay off technical debt
    * or else you will get to a place where you're only going to be doing that
    * is this doable in practice? how can you get a company to prioritize this? not really been able to see it done before
    * pitch that technical debt change as a "new idea" and give the stakeholder something that they will gain from it (saving money, faster development times, etc)
    * a lot of technical debt comes from bad programming practices - what standard is enough?
    * golden rule: leave the repo better than you found it
-dedicated team with very specific goals/measures of success to be able to get to a solution that can be measured
