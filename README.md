# Clean Code

## Chapter 1 (Clean Code)
This chapter tells us that even though some believe that code can disappear, the author tells us that it cannot, since the code itself represents the details of the requirements, these details cannot be ignored and must be specified and this is what the code is for. That however much the level of abstraction increases it will be a positive thing but it will not eliminate the code and he gives us a metaphor ; “Whoever thinks that the code will disappear is like the mathematician who hopes that one day mathematics will not be formal. They hope to discover a way to create machines that do what we want instead of what we say.”

In the first pages of the chapter we allude to the prologue of Implementation Patterns by Kent Beck where the importance of the correct code is highlighted, calling it: Fragile Premise . It tells us that the right code is relevant and that it has suffered by its absence. For this he gives us an example of a company in 1980 that launched an application that became popular but with a bug in the code that remained in future versions which increased the bugs and ended up disappearing. Then he tells us how two decades later he met one of the employees of that company and asked him questions about what had happened, in these answers it is given to understand that some reasons for which bad codes are written are caused by tight deadlines, fatigue or simply to leave it for later.


It explains the consequences of incorrect code and the disaster cycle. It tells us that when a project starts, everything moves fast but if you are not careful with the code in the future this error caused by an oversight could be unmanageable and cause progress to slow down, this leads to desperate decisions and hiring more people which worsens the situation. Teams demand to redo the whole design which creates tensions between old and new, even this new system could collapse if a clean code is not maintained, for this the chapter tells us to act as professionals keeping a clean code despite being under pressure and deadlines, for this it requires discipline and a sense of correctness.

To understand a little more and to see it from different perspectives, it shows us the vision of other renowned programmers:

Bjarne Stroustrup (Creator of C++):
- Elegance and efficiency: The code must be elegant, which implies grace, simplicity and nobility. It should also be efficient and not waste resources.
- Error handling: Careful attention to details such as avoiding inconsistent use of names or being careful with memory leaks.
- Functions and modules should focus on a single task, avoiding unnecessary complexity.

Grady Booch (Author of “Object-Oriented Analysis and Design”)
- Clean code should read like well-written text, without hiding the programmer's intent.
- Clear abstractions: It should have clear structures and be easy to follow, without introducing complexity.

Dave Thomas (Co-author of “The Pragmatic Programmer”)
- Clean code allows other programmers to easily understand and improve it. It also includes unit and acceptance tests, and uses meaningful names.
Michael Feathers (Author of “Working Effectively with Legacy Code”)
- Clean code gives the feeling of having been written by someone who cares. There seems to be nothing more that can be done to improve it.

Ron Jeffries (Pioneer of Extreme Programming).
Simple code according to Beck:
- Runs all tests.
- It has no duplication.
- Expresses all system design concepts.
- Minimizes the number of entities (classes, methods, functions).

Ward Cunningham (Inventor of the Wiki and advocate of agile development)
- Clean code is easily understood and is just as you would expect, with no complications or surprises. In addition, the code appears to be tailored to the problem, reflecting the programmer's ability to adapt to the language in an elegant way.
 
Boy Scout rule this rule alludes to the fact that we must leave the camp cleaner than what has been found, that is to say, leave the code cleaner than what we have received.
Clean code is not only functional, but also cares about how the rest can see it, if it is understandable and easy to maintain.
  

## Chapter 2 (Meaningful names)

This chapter talks about the importance of creating correct names and how we must create correct names.

The names must be explicit and must clarify why the variable exists, the function must provide enough information to know what it does and how it is used. This avoids the need for additional comments and improves code compression.

An essential rule is not to use confusing names, such as words with other common or technical meanings or similar names with minimal variations (hp instead of hypotenuse). And avoid terms that are used for specific things like List , if you are not using a list.

Avoid series of names like a1 or a2 or terms that are used for other things like Data or Info, the name must make sense and must have clarity, use descriptive and coherent names. It is also key to use names that can be pronounced to facilitate communication between programmers.

## Chapter 3 (Functions)

In this chapter it is mentioned that programming has evolved from routines and subroutines to the functions that today are.

It shows us an example of a normal code and a refactored code, you can see how thanks to this simplification a shorter and more understandable code is visualized.

It also tells us that an ideal code should be small, that more or less have 20 lines and that if we follow this rule so to speak we will have functions easier to understand. It is made clear that functions should perform a defined action and avoid multiple levels of abstraction within the same function.

In the same way it is indicated the use of switch instructions, as well as functions, these should be small and it is recommended to hide the switch logic in an abstract factory and prevent anyone to see it.

The functions must also have a good name, this must be descriptive and must help to understand the purpose of the function.

It tells us about the arguments, it tells us that if a function has no arguments it is better because it simplifies the understanding and testing, there are also the monodic of a single argument, these are easy to handle and remains understandable, however with the dyadic and triadic increases the complexity and are difficult to understand these should be avoided if possible and finally the polyadic (more than three) use them requires a justification because it is very complex. We must also keep in mind that a function must do what its name indicates, side effects such as changing the state of a session or modifying variables can be difficult to detect and generate confusing problems.

It is essential to use exceptions , instead of returning error codes , this allows us a cleaner error handling , try/catch blocks should be brief and when possible extract their logic in specific functions.

A very important thing is to avoid duplication in the code as this increases the complexity and the risk of errors. eliminating it is essential for a clean design, for that many design strategies are used, such as object oriented or structured programming. Dijkstra tells us that functions should have only one input and one output, this rule is useful but not necessary for small functions, a return, break or continue can improve clarity. Clean functions are not written on the first try, they are improved and reduced in complexity and tested to ensure correct operation.


## Chapter 4 (Comments)

In this chapter we will see the use of comments in the source code, telling us that this should be the last resort, as it indicates that the code should be self-explanatory and we emphasize that these can be beneficial or detrimental.

Comments are a sign of failure, an indication that the code is not clear or expressive enough. As the code changes, the comment may become outdated, which can lead to misinterpretation and cause misinformation. Although we discourage their excessive use we are given certain cases where they may be necessary:
- Legal: For example, copyright comments that cannot be avoided.
- Informative: When it is necessary to clarify aspects that are not obvious, these comments can be useful, but it is better to use the name of the function to convey the information whenever possible.
- Explaining intent: When design decisions are not obvious.
- Clarification: When function arguments need to be translated to improve understanding.
- Warning about consequences: When code behavior may not be obvious and have unexpected implications.

During the chapter it is emphasized that we should improve the code instead of adding comments, we are told that it is preferable to invest time in refactoring the code to make it clearer, to do this we are advised to use more expressive function names or clear design patterns to reduce the need for comments.

During refactoring, placeholders and brace comments should preferably be removed as they are often unnecessary in short functions. Comments such as assignments or mentions should not be included in the code as this information is already managed by version control. It is unnecessary to include html tags in comments, as it will complicate the reading and these should only be handled in the presentation of comments, besides commenting unnecessary details.

Comments should be used sparingly and it is much preferable to refactor so that the code is cleaner and clearer, eliminating the need for most comments, this should only be used when they provide explanatory value and is completely necessary.

## Chapter 5 (Format)

In this chapter we will see the importance of a good code format. For this we will see two formats: vertical and horizontal. Vertical: The code should follow a newspaper-like structure with a clear name and a logical flow, ideally it should have a maximum of 500 lines. Blank lines should be used to separate concepts, related lines should appear together, without unnecessary interruptions such as comments, and concepts should be close together to avoid the reader having to look for connections throughout the file.

Local variables should be declared as close as possible to their use, generally they should be placed at the top of the class to make it easier to find them.

At the same time, the dependent functions should be close to each other and the invoking function should be above the invoked ones, this will help to maintain coherence and clarity.

Horizontal Format: In this format the lines should not exceed 120 characters to avoid the need to scroll, the spacing should logically separate the elements and the spaces of the operators should be adjusted, improving the readability of the mathematical expressions. We must take into account the alignment of variables or assignments to form visually attractive columns is neither feasible nor advisable , it is preferable to leave variables and assignments unaligned .

The hierarchy of the code is shown with indentation, this helps programmers understand the context of the control structure and code blocks, disregarding the rules of indentation can reduce clarity and make it harder for others to decipher. It is important that teams agree on a set of rules for code formatting as this will help maintain consistency throughout the project and avoid unintelligible code with different styles.

## Chapter 7 (Processing errors)


In this chapter we will see how to manage errors in the code. For this we will turn to the use of exceptions instead of returned code, exceptions allow us to highlight the main logic of error handling, making the code more compressible. Exceptions define a transactional scope in the code, where it is better to define this scope first rather than adding additional logic, we suggest using TDD (Test Driven Development) to force exceptions and then develop the proper handling.

Checked exceptions offer advantages but also a high maintenance burden. We suggest avoiding checked exceptions in standard applications because the maintenance cost is high.

We must also keep in mind that the exceptions must be clear and sufficient about the error, including details about the failed operation and the type of failure, this will help to have a better diagnosis and logs of these errors, it is important to design exception classes considering how they are captured, this approach helps us to improve encapsulation and facilitates the replacement of external APIs.

We must keep in mind that returning null will increase complexity, since it forces invokers to perform constant checks to avoid exceptions such as NullPointerException, we are recommended to return default objects or throw clear exceptions and passing null as arguments can also be problematic, this should be avoided and instead throw exceptions or use assertions to avoid errors. The best practice is to design code that assumes that null is not a valid value.
