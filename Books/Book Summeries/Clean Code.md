https://betterprogramming.pub/thoughts-on-clean-code-d373c0d93ea4
The Clean Approach To Coding
You Will Probably Be the Next Person To Read the Code You Are Writing — Do Your Future Self a Favor
Although developers write code for their profession, they do a fair amount of reading code as well. In fact, most developers do more reading than actual coding.
How many times have you read the code you have just written? Obviously, the ratio is in favor of reading than of actual coding.
If most of our time is spent on understanding and reading code, we better make sure that when we actually code, it will be unambiguous to all our peers.

Since you will probably be the next person to read the code you are writing, make sure you will understand it even two months from now. I am sure almost every programmer (at least me) has written code at 3 AM just to wake up the next day and spend hours trying to figure what is going on.
Making sure your code is clear and clean will minimize the WTF moments, enhance your productivity, and will have lasting results in the long term. Do yourself a favor, and start writing clean code.
There Are More Parameters To Code Than “Works” vs. “Doesn’t Work”
Code should not be measured on solely “works” or “doesn’t work”. Of course, code that doesn’t work is not good —because it doesn't work.
But code that does work is not necessarily good, and that is a very important distinction to make. Once our code proves to work, our job as developers is not done.
A professional developer makes sure that after the code passes all the tests, it is also clear, clean, and maintainable. The actual principles of how to write clean code will follow, but for now, we must not judge code only by its workability.
There are more parameters and guiding principles to what is a well-written piece of code.
Better Clear Than Clever
As software engineers, we engage in problem-solving, creativity, and intensive thinking. Many times, when encountered with complex problems, our code can turn out to be “clever”- as in, doing very smart things that only the person that has written the code can understand what the heck is going on.
That is an undesirable outcome, even when the problem is tough to solve.
True mastery and professionalism are to solve a complex problem and showcase its solution cleanly and clearly so that other people will be able to review the code and be involved in it. It is not because we need to be nice to our colleagues and share with them the fun (although that is also a good reason), rather than if you are the only person to understand the code it will harm you in the long term.
Your colleagues will not only have a tough time refactoring the code, but it will also constrain the project and make it slower — and you’ll be attached to a piece of code forever until you die or leave the company.
We must make sure that after we solve a problem, the solution will seem clear and simple to anyone that reads that piece of code.
Anticipation and Trust Are Crucial
When someone reads your code, there is a process of building trust between you and the reader. Trust is basically conveyed to confidence. The reader has some degree of confidence in the code you have written, and when the confidence is high the project can move faster.
I hope it is clear by now that the reader is also your future self. If you do not trust your own code, then good luck to you.

So, how can we build trust and confidence with the reader? By letting them anticipate correctly what is going to happen. Once the reader understands the code, knows what the code is supposed to do, and correctly anticipates what will come next, trust is built between the sides.
Prevent surprises, unclarity, and ambiguous code that might confuse the reader. If a function or a class is anticipated to do a certain action, but the reader is surprised and other actions are done — the confidence is shaken and the reader cannot trust the programmer anymore, how could they? They were wrong on this piece of code, and now they will be in a constant guessing mode throughout the whole review.
Clean Code Does Not Happen at Once, by Itself
Now that we have laid out why clean code is crucial to our success as developers, we are faced with the fatal question:
How do I write clean code?
Well, it surely doesn’t happen by itself. it requires practice, continuous iterations, and refactoring, and constantly adhering to the principles of clean code. Uncle Bob clearly mentions that even he doesn't write clean code the first time. every piece of code is examined after it is written and refactored to adhere to the principles of clean code.
Timeless principles
Separate Concerns
Each section in the code should deal with a certain concern of the software. Writing functions or classes that involve distinctive concerns is not an example of clean code. Instead, keep the business logic separated. Whether we are talking in terms of modules, classes, functions — each in its own level of abstraction.
Yet, the principle is straightforward: What is the logic I am writing now? What is the main concern here? Do I have other concerns that are implemented? If you do, separate them.
Code Is Like an Article
An article, or a blog, has a clear structure. The main subject is at the top, and as we proceed with the article we can notice that the main subject is broken into subparts, and within them, we have more details regarding each part.
Code should follow the same principle.
In the beginning, we will have the main concern the piece of code is dealing with. As we progress, the function and classes will entail more details of implementation and keep a clear separation of concerns — exactly like each blog has a sub-header and a paragraph that is tightly related to it.
Each piece of code should be broken into classes and functions that deal with a specific concern, and as we proceed within them, they deal with that concern only
The Boy Scout Rule
When I was at the boy scouts, I was an instructor of kids with special needs. Our guiding principle when we went on field trips was “leave the place cleaner than you found it”.
Apparently, Uncle Bob in his book feels pretty much the same way about code — Always leave the code better than you found it. As discussed before, clean code is a process. It consists of continuous improvement and development, by you and by others in the organization.
Therefore, leave the code better than you found it. Bad variable names, useless comments, commented out code — the longer it stays, the smellier it gets. Be proactive. Be a boy scout.
Clean, Reusable, and Maintainable
Always make sure your code follows these guidelines. By making sure it does, you check off most of the principles of the book.
Clean code is code that has a good structure, is clear, well named, and does not contain surprises.
Reusable code forces you to separate concerns, keep the correct level of abstraction, and prevents you from writing code that is logically dependent on other sections(more on that later).
Maintainable code allows others to contribute and understand what is going on. It takes into account that software transforms with time. Therefore, anticipate changes and make sure that the code will be easy to refactor if changes happen.
Never Duplicate
Duplication means for a fact that the code is not clean. Follow the DRY principle — Don’t Repeat Yourself. Duplication cries for a function, class, component- whatever! just don’t duplicate!
Whenever you find yourself doing the slightest ctrl+c and ctrl+v sequence, intuitively ask yourself if there is a better option. Most of the time, the answer will be a definitive YES.
Avoid Logical Dependency
Logical dependency means that a piece of code is relying on a separated piece of code to contain certain business logic, assuming that the code won’t change and therefore the implementation is fine.
When we write code, we must make sure that the code is “on its own” — that we have the correct level of abstraction, that the code doesn’t know pieces of information it is not supposed to know (based on its level of abstraction and concern) and that if the code is refactored, we will not have an unusual amount of side effects in other function and classes as well.
Naming
Choose Descriptive and Unambiguous Names
Names should describe what is done or contained. Part of being clear is not letting any other interpretation for the name and directing the reader to only one possible conclusion.

Notice that the example below does not require any commenting or explanation of any sort. it is descriptive and leads to one conclusion only.
// BAD
let days;// elapsed time in days 
//CLEAN 
let daysSinceCreation;
let daysSinceUpdate;
let ageInDays;
let elapsedDays;
Make Meaningful Distinctions
It is important to have names that are distinct in context and structure. For obvious reasons, we do not want to confuse the context and meaning of one variable/function with the other.
However, they mustn't have a very similar name as well.
// Not distincting context 
getActiveAccount();
getActiveAccountInfo();
getActiveAccountData();
In the example above, it is not sure what the distinction is between Account, AccountInfo, and AccountData. They say pretty much the same thing. What is data? What is the info? What is account if not account data and how are they different? So many questions from these ambiguous names.
// Not disticnting structure
getActiveAccount()
getActiveAccounts()
getActivityAccount()
//With distinction 
getActiveAccount()
getManyActiveAccounts()
getAccountActivity()
The autocomplete feature in all code editors should be taken into account as well. Having very similar names is prone to autosuggestion mistakes, improper reading, and consequentially — incorrect functions being called.
Use Searchable Names
While we name variables in our code, we must make sure that they are not encoded, too short (1–2 letters), and not too common — depending on their significance and scope.
In the example that follows, the app is a course management platform for students.
//Bad examples
const max=7;
const students=7;
//Clean example
const MAX_CLASSES_PER_STUDENT=7;
I don’t think you will have any trouble finding that variable, whereas max and students are very likely to be common words in this app
No Magic Values
Magic values are values that “magically” appear in the code and are supposed to convey some meaning, yet no one can tell since they are just numbers/strings.
Avoid sprinkling magic values throughout the code at all costs. Make sure to assign a variable to these values for clarity and easy refactoring.
//BAD 
if(val === 38) console.log('congratulations!')
//CLEAN
const JACKPOT=38;
if(val === JACKPOT) console.log('congratulations!')
Do Not Disclose Implementation
The way we implement code differs from time to time and transforms altogether. Binding a certain way of implementation is constraining and in effect will become obsolete when time passes by.
//BAD 
spliceProductFromArr()
let productArr=[]; 
//CLEAN 
removeProductById()
let products=[];
Beware of Naming Conventions
If we are developing an app that is mainly related to cars, what will be our naming convention? Car? Vehicle? Automobile? Whichever it is, please consider car to be consistent.
The chosen name should be referenced in the functions, variables, services, classes — whenever needed. Yet, synonyms are very confusing so choose a one-word convention and stick with it.
Avoid Mental Mapping
Variables that require the reader (and coder ) to remember their meaning are generally bad variable names. The only exception that comes to mind is i and j which are iterators in a loop.
Besides that, names should reflect reality, be consistent and descriptive enough to avoid any mental mapping or memorization of any kind.
Functions
Should Be Small
Small functions help you tell the story correctly. They add to order, separation of concerns, proper abstraction, and correct structure to your code.
If your function is not small, it is probably not following other crucial principles we will discover shortly. Small functions, when named correctly, make the code clear, easy to debug, and simple to follow.
How Small? You might wonder. Well, according to the author of Clean Code, Uncle Bob, a function should never be more than 20 lines of code.
If it is, according to Bob, then you can probably split it into another function. Regarding the exact number, I am sure it is just a thumb rule or a red flag to keep us alert if we write large functions.
“The first rule of functions is that they need to be small. The second rule is that they need to be smaller than that.”
Does One Thing
Functions should do one thing, and one thing only. Sometimes, it is very difficult to make sure that the function does only one thing, yet it is an important principle to make sure we are not doing multiple things at once. Bob’s rule? If it’s doing more than one thing then you probably have 2 functions, not one.
“Functions should do one thing.They should do it well.They should do it only”
Should Be Named Properly
All functions do actions. that is the purpose of them - to function. Therefore, when naming functions, they should have verbs entailing what they do.
get, set, save, remove, load… you get the gist of it, right?
One common exception, however, which is widely known, is the word is — to check for a boolean condition.
The convention is that the function shall return a boolean regarding the condition (no surprises with the wrong anticipation). So, an invalid password(password) is anticipated to return a boolean.
Should Minimize Arguments
Ideally, the lesser the arguments the better. However, if we want to make our functions reusable and independent of any other business logic, some arguments might be needed.
Therefore, up to 2 arguments is fine, 3 should be avoided, and beyond that invited hard probing. The idea behind this principle is that functions are anyway very small, so if you need 3 arguments that are vital to the business logic, probably the decoupling of the grand function was done poorly.
Meaning, the logic is tied too strongly together, and maybe separation in a different point in the code is better.
Do Not Create Side Effects
Functions should not have any side effects or implications on other processes, other than its main responsibility. As the “Do One Thing” rule suggests, it should not do anything else besides its designated task to do.
This helps prevent surprises, it is easier to debug and to keep track exactly of what does what.
The Clean Way To Write Functions
Let’s admit it. It is very hard to write functions that adhere to these principles on our first try. We will likely overthink and do much more planning than we need to to get it on our first try.
But the truth is, it is not supposed to be perfect the first time we write the function. Just like in writing, coding has its layers, drafts, refinements (refactoring), and development until it is sharp and shiny. Uncle Bob puts it eloquently :
“Writing software is like any other kind of writing.when you write a paper or an article, you get your thoughts down first,then you massage it until it reads well. The first draft might be clumsy and disorganized, do you wordsmith it and restructure it and refine it until it reads the way you want it to read”
Classes
Should Be Small
The first rule of classes is that they need to be small. The second rule is that they need to be smaller than that. Sounds familiar? Classes should follow the same principle as functions — make them as small as you can.
There is, however, one small distinction — classes may do more than one thing. They will probably do more than one thing most of the time. That being said, they must follow the Single Responsibility Principle
The Single Responsibility Principle
Classes should have one responsibility, and nothing more than that. This is where the separation of concerns is an actual concern… as developers, we must make sure that classes have only one responsibility to create small and clean classes.
Responsibility is a term that in this context means a reason to change. There should be only one reason for the class to change. if multiple reasons can cause the class to change, it means that the class has too many responsibilities. This is a concise way of making sure that the class has a single responsibility.
Cohesion
How well is the logic within a class “glued” together and has connecting dots within it? How well are the methods implemented with the logic and the class and are they in the proper place?
A good indicator that might help answer these questions is the number of instance variables in a class. Ideally, we would prefer to reduce the number of instance variables and use each of them in the methods of the class. That is cohesion in a class.
The methods are strongly related to the class, they use the instance variables and the logic is cultivated and used by all the methods. This is a strong indicator that all the methods and concerns are in the right place.
“the strategy of keeping functions small and keeping parameter lists short can sometimes lead to a proliferation of instance variables that are used by a subset of methods.When this happens, it almost always means that there is at least one other class trying to get out of the larger class. You should try to separate the the variables and methods into two or more classes such that the new classes are more cohesive”
General Concepts For Clean Code
The Best Comment Is the Comment You Didn’t Write
Comments in code, excluding technical aspects, are to be mitigated as much as possible. They are hard to maintain, they usually try to cover up to code that is not clean enough.
If you feel a need to write a comment that explains what the code does, that should raise a red flag and you should scrutinize your code and make sure it is clean enough.
We are not referring to comments that are part of a library’s documentation, nor technical comments of licensing.
Comments should be mitigated. The leading principle is that if you need to explain what the code does, the code is not clear enough. Code should explain itself by itself. It should be self-explanatory for other peers to review.
Understand the Algorithm
Understanding the algorithm is a crucial step in writing clean code. Beyond the obvious reasons why we need to understand the algorithm, one can write clean code only if he understands it truly.
If we invest time in learning the algorithm and making sure we know its intricacies, we will be able to deconstruct it into smaller parts. From there, the path to writing clean code is fairly straightforward
our ability to write clean code is derived from our comprehension of the algorithm and choosing the precise poits to deconstruct it to smaller parts
Beware of Abstraction Levels
An abstraction level is an important concept to consider when planning and writing code. While we write a function, we consider where it stands in the grand scheme of the solution.
Is it a high-level function this is closely related to the algorithm? Or is it a function that is responsible for a utility purpose (like parsing a command line, checking conditionals, performing certain calculations)?
The abstraction level principle is another way of making sure we are keeping all our functions and classes in place and that our functions are doing one thing only. If a function mixes levels of abstraction it definitively is doing more than one thing.
Thinking in terms of abstraction is a tool to help us organize better the structure of the functions and to plan how the whole puzzle is assembled.
To get practical, we will always start with the higher-level functions that are at the highest level of abstraction. Each function shall descend only one level below while it calls the other function.
As we have covered already, the granular details of the algorithm and the specific implementation will be uncovered further down the source code.
The leading question is what do I care about in this logic? Of course, we care about every single line. Yet, what is the imperative bulk of the algorithm, where the main logic is contained? That is the highest level of abstraction.
The orchestration of the whole logic. Boundry checking, error handling, parsing, calculations — they are at a different level of abstraction. They should be extracted to different functions, each dealing with its own level of abstraction.
Consider the following code :
//Mongoose call to create a product
async function createProduct(productToSave) {
  try {
    const product = new Product(productToSave)
    return await product.save()
  } catch (e) {
    _handleError('failed to create product in db', e)
}
}
Did you notice the _handleError function? Besides pointing exactly what was the error, the function createProduct has no idea how the error is being handled. It is just passing along the error and letting a different function at a lower level of abstraction.
Why is that? Because it is not its responsibility. The function gets a product and returns a saved product from the DB. Errors? great. Not its responsibility. It activates the _handleError function to do exactly what its title concludes: To handle errors.
function _handleError(msg, e = 'initiated') {
    logger.error(msg, e)
    throw Error(msg, e)
}
Does the function above have any idea what the logger does with the error? Not at all.
As we have probably understood, it is not its job to log the error. Its job is to handle the error — call the relevant functions at the next lower level of abstraction and pass along the information
Final Word: Be Consistent
To conclude, I believe this is a recipe for clean code and being a great programmer. Everybody has their own style, unique point of view, and a different approach to solving problems.
Therefore, being consistent with all the principles mentioned in this article is key to being able to write maintainable, reusable, clear, and clean code.
Good Luck!