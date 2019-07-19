
# Clean Code: A Handbook of Agile Software Craftsmanship 1st Edition

## Author: Robert C. Martin


## Ch1-2: Clean Code & Meaningful Names
-Clean code does one thing well.
Clean code is focused. Each function, each class, each module exposes a single-minded attitude that remains entirely undistracted, and unpolluted, by the surrounding details.
-Clean code can be read, and enhanced by a developer other than its original author. It has unit and acceptance tests. It has meaningful names. It provides one way rather than many ways for doing one thing. It has minimal dependencies, which are explicitly defined, and pro- vides a clear and minimal API. Code should be literate since depending on the language, not all necessary information can be expressed clearly in code alone.
-Clean code always looks like it was written by someone who cares.
-You can call it beautiful code when the code also makes it look like the language was made for the problem.
-Leave the campground cleaner than you found it.

## Ch 3-4: Functions & Comments
-the first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that.
-the blocks within if statements, else statements, while statements, and so on should be one line long. Probably that line should be a function call
-FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY - If a function does only those steps that are one level below the stated name of the function, then the function is doing one thing.
-Mixing levels of abstraction within a function is always confusing. Readers may not be able to tell whether a particular expression is an essential concept or a detail. Worse, like broken windows, once details are mixed with essential concepts, more and more details tend to accrete within the function.
-Making the code read like a top-down set of TO paragraphs is an effective technique for keeping the abstraction level consistent.
-bury the switch statement in the basement of an ABSTRACT FACTORY,9 and never let anyone see it
-The ideal number of arguments for a function is zero (niladic). Next comes one (monadic), followed closely by two (dyadic). Three arguments (triadic) should be avoided where possible. More than three (polyadic) requires very special justification—and then shouldn’t be used anyway.
-Passing a boolean into a function is a truly terrible practice. It immediately complicates the signature of the method, loudly proclaiming that this function does more than one thing. It does one thing if the flag is true and another if the flag is false!
-Reducing the number of arguments by creating objects out of them may seem like cheating, but it’s not. When groups of variables are passed together, the way x and y are in the example above, they are likely part of a concept that deserves a name of its own.
-Side effects are lies. Your function promises to do one thing, but it also does other hidden things.
-Functions should either do something or answer something, but not both.
-it is better to extract the bodies of the try and catch blocks out into functions of their own.
-Functions should do one thing. Error handing is one thing. Thus, a function that handles errors should do nothing else.
-Writing software is like any other kind of writing. When you write a paper or an article, you get your thoughts down first, then you massage it until it reads well. The first draft might be clumsy and disorganized, so you wordsmith it and restructure it and refine it until it reads the way you want it to read.
-Every system is built from a domain-specific language designed by the programmers to describe that system. Functions are the verbs of that language, and classes are the nouns.
-Nothing can be quite so helpful as a well-placed comment. Nothing can clutter up a module more than frivolous dogmatic comments.
-The proper use of comments is to compensate for our failure to express ourself in code. Note that I used the word failure. I meant it. Comments are always failures.
-Inaccurate comments are far worse than no comments at all. They delude and mislead. They set expectations that will never be fulfilled. They lay down old rules that need not, or should not, be followed any longer.
-Clear and expressive code with few comments is far superior to cluttered and complex code with lots of comments. Rather than spend your time writing the comments that explain the mess you’ve made, spend it cleaning that mess.
-// Check to see if the employee is eligible for full benefits if ((employee.flags & HOURLY_FLAG) && (employee.age > 65)) Or this? if (employee.isEligibleForFullBenefits())
-There is nothing quite so helpful and satisfying as a well-described public API.
-required javadocs for every function lead to abominations such as List- ing 4-3. This clutter adds nothing and serves only to obfuscate the code and create the potential for lies and misdirection.
-/*** Returns the day of the month. ** @return the day of the month. */ public int getDayOfMonth() { return dayOfMonth; }
-Replace the temptation to create noise with the determination to clean your code. You’ll find it makes you a better and happier programmer.
-Others who see that commented-out code won’t have the courage to delete it. They’ll think it is there for a reason and is too important to delete. So commented-out code gathers like dregs at the bottom of a bad bottle of wine.
-DRY - don’t repeat yourself lol

## Ch 5-6: Formatting & Objects/Data Structures
-We want them to be struck by the orderliness. We want their eyebrows to rise as they scroll through the modules. We want them to perceive that professionals have been at work. If instead they see a scrambled mass of code that looks like it was written by a bevy of drunken sailors, then they are likely to conclude that the same inattention to detail pervades every other aspect of the project.
-A newspaper is composed of many articles; most are very small. Some are a bit larger. Very few contain as much text as a page can hold. This makes the newspaper usable. If the newspaper were just one long story containing a disorganized agglomeration of facts, dates, and names, then we simply would not read it.
-If openness separates concepts, then vertical density implies close association. So lines of code that are tightly related should appear vertically dense.
-Have you ever hunted up the chain of inheritance for the definition of a variable or function? This is frustrating because you are trying to understand what the system does, but you are spending your time and mental energy on trying to locate and remember where the pieces are.
-The important thing is for the instance variables to be declared in one well-known place. Everybody should know where to go to see the declarations.
-If one function calls another, they should be vertically close, and the caller should be above the callee, if at all possible. This gives the program a natural flow. If the convention is followed reliably, readers will be able to trust that function definitions will follow shortly after their use.
-In general we want function call dependencies to point in the downward direction. That is, a function that is called should be below a function that does the calling.2 This creates a nice flow down the source code module from high level to low level.
-This suggests that we should strive to keep our lines short. The old Hollerith limit of 80 is a bit arbitrary, and I’m not opposed to lines edging out to 100 or even 120. But beyond that is probably just careless.
-Nowadays I prefer unaligned declarations and assignments, as shown below, because they point out an important deficiency. If I have long lists that need to be aligned, the problem is the length of the lists, not the lack of alignment.
-To make this hierarchy of scopes visible, we indent the lines of source code in pro- portion to their position in the hierarchy.
-Every programmer has his own favorite formatting rules, but if he works in a team, then the team rules.
-Hiding implementation is not just a matter of putting a layer of functions between the variables. Hiding implementation is about abstractions! A class does not simply push its variables out through getters and setters. Rather it exposes abstract interfaces that allow its users to manipulate the essence of the data, without having to know its implementation.
-This exposes the fundamental dichotomy between objects and data structures: Procedural code (code using data structures) makes it easy to add new functions without changing the existing data structures. OO code, on the other hand, makes it easy to add new classes without changing existing functions. The complement is also true: Procedural code makes it hard to add new data structures because all the functions must change. OO code makes it hard to add new functions because all the classes must change.
-There is a well-known heuristic called the Law of Demeter2 that says a module should not know about the innards of the objects it manipulates. More precisely, the Law of Demeter says that a method f of a class C should only call the methods of these: •C • An object created by f  • An object passed as an argument to f • An object held in an instance variable of C. The method should not invoke methods on objects that are returned by any of the allowed functions. In other words, talk to friends, not to strangers.
-The quintessential form of a data structure is a class with public variables and no functions. This is sometimes called a data transfer object, or DTO.
-Objects expose behavior and hide data. This makes it easy to add new kinds of objects without changing existing behaviors. It also makes it hard to add new behaviors to existing objects. Data structures expose data and have no significant behavior. This makes it easy to add new behaviors to existing data structures but makes it hard to add new data structures to existing functions.

## Ch 7-8: Error Handling & Boundaries
-The code is better because two concerns that were tangled, the algorithm for device shutdown and error han- dling, are now separated. You can look at each of those concerns and understand them independently.
-When you wrap a third-party API, you minimize your dependencies upon it: You can choose to move to a different library in the future without much penalty. Wrapping also makes it easier to mock out third-party calls when you are testing your own code.
-When we return null, we are essentially creating work for ourselves and foisting problems upon our callers. All it takes is one missing null check to send an application spinning out of control.
-Unless you are working with an API which expects you to pass null, you should avoid passing null in your code whenever possible.
-If you use a boundary interface like Map, keep it inside the class, or close family of classes, where it is used. Avoid returning it from, or accepting it as an argument to, public APIs.
-Not only are learning tests free, they have a positive return on investment. When there are new releases of the third-party package, we run the learning tests to see whether there are behavioral differences.
-Interesting things happen at boundaries. Change is one of those things. Good software designs accommodate change without huge investments and rework. When we use code that is out of our control, special care must be taken to protect our investment and make sure future change is not too costly.
-Code at the boundaries needs clear separation and tests that define expectations. We should avoid letting too much of our code know about the third-party particulars. It’s better to depend on something you control than on something you don’t control, lest it end up controlling you.
-We manage third-party boundaries by having very few places in the code that refer to them.

## Ch 9-10: Unit Tests & Classes
-First Law You may not write production code until you have written a failing unit test. Second Law You may not write more of a unit test than is sufficient to fail, and not compiling is failing. Third Law You may not write more production code than is sufficient to pass the currently failing test.
-What this team did not realize was that having dirty tests is equivalent to, if not worse than, having no tests. The problem is that tests must change as the production code evolves. The dirtier the tests, the harder they are to change. The more tangled the test code, the more likely it is that you will spend more time cramming new tests into the suite than it takes to write the new production code.
-The moral of the story is simple: Test code is just as important as production code. It is not a second-class citizen. It requires thought, design, and care. It must be kept as clean as production code.
-It is unit tests that keep our code flexible, maintainable, and reusable. The reason is simple. If you have tests, you do not fear making changes to the code! Without tests every change is a possible bug.
-What makes a clean test? Three things. Readability, readability, and readability.
-That is the nature of the dual standard. There are things that you might never do in a production environment that are perfectly fine in a test environment. Usually they involve issues of memory or CPU efficiency. But they never involve issues of cleanliness.
-I think the best thing we can say is that the number of asserts in a test ought to be minimized. Perhaps a better rule is that we want to test a single concept in each test function.
-Clean tests follow five other rules that form the above acronym: Fast Tests should be fast. They should run quickly. Independent Tests should not depend on each other. Repeatable Tests should be repeatable in any environment. You should be able to run the tests in the production environment, in the QA environment, and on your laptop while riding home on the train without a network. Self-Validating The tests should have a boolean output. Either they pass or fail. You should not have to read through a log file to tell whether the tests pass. Timely The tests need to be written in a timely fashion. Unit tests should be written just before the production code that makes them pass.
-The first rule of classes is that they should be small. The second rule of classes is that they should be smaller than that.
-With functions we measured size by counting physical lines. With classes we use a different measure. We count responsibilities.
-The name of a class should describe what responsibilities it fulfills. In fact, naming is probably the first way of helping determine class size.
-The Single Responsibility Principle (SRP) states that a class or module should have one, and only one, reason to change.
-However, a system with many small classes has no more moving parts than a system with a few large classes. There is just as much to learn in the system with a few large classes. So the question is: Do you want your tools organized into toolboxes with many small drawers each containing well-defined and well-labeled components? Or do you want a few drawers that you just toss everything into?
-For most systems, change is continual. Every change subjects us to the risk that the remainder of the system no longer works as intended. In a clean system we organize our classes so as to reduce the risk of change.
-Classes should be open for extension but closed for modification.
-By minimizing coupling in this way, our classes adhere to another class design principle known as the Dependency Inversion Principle (DIP).5 In essence, the DIP says that our classes should depend upon abstractions, not on concrete details.

