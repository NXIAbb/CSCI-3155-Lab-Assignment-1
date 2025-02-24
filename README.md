Download Link :https://programming.engineering/product/csci-3155-lab-assignment-1/


# CSCI-3155-Lab-Assignment-1
CSCI 3155: Lab Assignment 1
The purpose of this assignment is to warm-up with Scala and to refresh preliminaries from prior courses.

Learning Goals. The primary learning goals of this lab are to build intuition for the following:

thinking in terms of types, values, and expressions;

representing data structures as algebraic data types; and

representing programs as abstract syntax trees.

PL Ideas Abstract syntax. Expressions conforming to types and evaluating to values.

FP Skills Data structures as algebraic terms.

General Guidelines. The instructor will randomly assign partners for the lab assignment, and you will get a different partner for every lab assignment. You will work on this assignment closely with your partner. However, note that each student needs to submit on Canvas and are individually responsible for completing the assignment so that you can do well in your in-terview.

You are welcome to talk about these questions beyond your teams. However, we ask that you code in pairs. See the collaboration policy for details, including the following:

Bottom line, feel free to use resources that are available to you as long as the use is rea-sonable and you cite them in your submission. However, copying answers directly or indirectly from solution manuals, web pages, or your peers is certainly unreasonable.

Also, recall the evaluation guideline from the course syllabus.

Both your ideas and also the clarity with which they are expressed matter—both in your English prose and your code!

We will consider the following criteria in our grading:


How well does your submission answer the questions? For example, a common mistake is to give an example when a question asks for an explanation. An example may be useful in your explanation, but it should not take the place of the explanation.

How clear is your submission? If we cannot understand what you are trying to say, then we cannot give you points for it. Try reading your answer aloud to yourself or a friend; this technique is often a great way to identify holes in your reasoning. For code, not every program that “works” deserves full credit. We must be able to read and understand your intent. Make sure you state any pre-conditions or invariants for your functions (either in comments, as assertions, or as require clauses as appropriate).

Try to make your code as concise and clear as possible. Challenge yourself to find the most crisp, concise way of expressing the intended computation. This may mean using ways of ex-pression computation currently unfamiliar to you.

Finally, make sure that your file compiles and runs via sbt test. A program that does not compile will not be graded—no interview will be conducted.

Submission Instructions. We are using GitHub for assignment distribution and auto-testing. You need to have a GitHub identity and must have your full name in your GitHub profile so that we can associate you with your submissions.

You will be editing and submitting the the following files:

src/main/scala/jsy/student/Lab1.scala with your solution to the coding exercises;

src/test/scala/jsy/student/Lab1Spec.scala with your additional tests; and

lab1-writeup.pdf or lab1-writeup.md for a pdf or a Markdown document that should be pushed to the root directory of your repository with your response to the written ques-tions (scanned, clearly legible handwritten write-ups are acceptable). You will not get credit for write-ups in any other file format.

You are also likely to edit src/main/scala/jsy/student/Lab1.worksheet.sc for any scratch work.

Following good git practice, please make commits in small bits corresponding to completing small conceptual parts and push often so that your progress is evident. We expect that you have some familiarity with git from prior courses. If not, please discuss with your classmates and the course staff (e.g., via Piazza).

At any point, you may push your updated files to your GitHub repository for auto-testing. You need to push to your GitHub repository for the auto-testing part of your score, as well as to continue to the interview.

Sign-up for an interview slot for an evaluator. To fairly accommodate everyone, the inter-view times are strict and will not be rescheduled. Missing an interview slot means missing the interview evaluation component of your lab score. Please take advantage of your interview time to maximize the feedback that you are able to receive. Arrive at your interview ready to show


your implementation and your written responses. Implementations that do not compile and run will not be evaluated.

Finally, upload the zip file of your repo to Canvas by clicking the Code button and then Download ZIP. The generated file should be named your-lab-repo-name-main.zip.

Getting Started. First, form a team of two and pick a team name. For our bookkeeping, please prefix your team name with the lab number and your CU IdentiKeys (i.e., your team should look something like L1_your-identikey1_your-identikey2_anatomists).

You must work in teams of two, and you will form teams in lab section. If you cannot connect with your partner, then please contact the course staff (via Piazza).

Then, log into Canvas and follow the GitHub Classroom link for setting up your Lab 1 repos-itory with your team name. The first person will create the team, and the second person will select the team name from the existing team names. If you need to move teams after you have already created or joined a repository, you will need to contact the Course Manager (via Piazza) or work with a course staff member to move you manually.

If you would like to look at the code before getting your own copy from GitHub Classroom, you may go to https://github.com/csci3155/pppl-lab1.

Checkpoint. The checkpoint is to encourage you to start the assignment early and it requires you to submit (i.e., push) your partial solution on GitHub a week before the assignment is due. You do not need to attempt everything a week early, but we want you to start working on it and make note in this handout any required questions in the checkpoint. This means that submit-ting the empty template that fails all tests is not sufficient. Failing to submit to the checkpoint will prevent you from proceeding to the interview. However, as long as you pass the checkpoint, this early score from the checkpoint will not affect your grade for the assignment.

Development Environment. Once you have the project files, follow the instructions in the README.md for setting up your development environment.

Scala Practice. A suggested way to get familiar with Scala is to do some small lessons with Scala Koans (http://www.scalakoans.org/). For this lab, we suggest that you consider look-ing at the AboutAsserts, AboutLiteralBooleans, AboutLiteralNumbers, AboutLiteralStrings, About-Methods, AboutRecursion, AboutTuples, AboutCaseClasses, and AboutPatternMatching koans.

Feedback. Complete the survey linked from Canvas after completing this assignment. Any non-empty answer will receive full credit.

Scala Basics: Binding and Scope. For each the following uses of names, give the line where that name is bound. Briefly explain your reasoning (in no more than 1–2 sentences).

Consider the following Scala code.

def plus(x: Int, y: Int) = x + y

Yes, the body expression of plus is well-typed with type Int.

+ y : Int because

x : Int

y : Int

Run-Time Library. Most languages come with a standard library with support for things like data structures, mathematical operators, string processing, etc. Standard library func-tions may be implemented in the object language (perhaps for portability) or the meta lan-guage (perhaps for implementation efficiency).

For this question, we will implement some library functions in Scala, our meta language, that we can imagine will be part of the run-time for our object language interpreter. In actuality, the main purpose of this exercise is to warm-up with Scala.

Write a function abs

def abs(n: Double): Double

that returns the absolute value of n. This a function that takes a value of type Double and returns a value of type Double. This function corresponds to the JavaScript library function Math.abs.

Instructor Solution: 1 line.

A response to this question is required for the checkpoint.

(b) Write a function xor

def xor(a: Boolean, b: Boolean): Boolean

that returns the exclusive-or of a and b. The exclusive-or returns true if and only if exactly one of a or b is true. For practice, do not use the Boolean operators. Instead, only use the if–else expression and the Boolean literals (i.e., true or false).

Instructor Solution: 4 lines (including 1 line for a closing brace).

Run-Time Library: Recursion.

Write a recursive function repeat

def repeat(s: String, n: Int): String

where repeat(s, n) returns a string with n copies of s concatenated together. For example, repeat(“a”,3) returns “aaa”. This function corresponds to the function goog.string.repeat in the Google Closure library.

Instructor Solution: 4 lines (including 1 line for a closing brace).

In this exercise, we will implement the square root function—Math.sqrt in the JavaScript standard library. To do so, we will use Newton’s method (also known as Newton-Raphson).

Recall from Calculus that a root of a differentiable function can be iteratively approxi-mated by following tangent lines. More precisely, let f be a differentiable function, and

let x0 be an initial guess for a root of f . Then, Newton’s method specifies a sequence of approximations x0, x1, . . . with the following recursive equation:1

f (xn )

xn+1 = xn − f ′(xn ) .

The square root of a real number c for c > 0, written c, is a positive x such that x2 = c. Thus, to compute the square root of a number c, we want to find the positive root of the function:

(x) = x2 −c .

Thus, the following recursive equation defines a sequence of approximations for c:

x2 −c

n

xn+1 = xn − .

2xn

i. First, implement a function sqrtStep

def sqrtStep(c: Double, xn: Double): Double

that takes one step of approximation in computing c (i.e., computes xn+1 from xn ).

Instructor Solution: 1 line.

ii. Next, implement a function sqrtN

def sqrtN(c: Double, x0: Double, n: Int): Double

that computes the nth approximation xn from an initial guess x0. You will want to call sqrtStep implemented in the previous part.

Challenge yourself to implement this function using recursion and no mutable variables (i.e., vars)—you will want to use a recursive helper function. It is also quite informative to compare your recursive solution with one using a while loop. Instructor Solution: 7 lines (including 2 lines for closing braces and 1 line for a require).

iii. Now, implement a function sqrtErr

def sqrtErr(c: Double, x0: Double,

epsilon: Double): Double

that is very similar to sqrtN but instead computes approximations xn until the approximation error is within ε (epsilon), that is,

|xn2 −c| < ε .

You can use your absolute value function abs implemented in a previous part. A wrapper function sqrt is given in the template that simply calls sqrtErr with a choice of x0 and epsilon.

1The following link is a refresher video on this algorithm: http://www.youtube.com/watch?v=1uN8cBGVpfs, January 2012

Again, challenge yourself to implement this function using recursion and compare your recursive solution to one with a while loop.

Instructor Solution: 5 lines (including 1 line for a closing brace and 1 line for a

require).

Data Structures Review: Binary Search Trees.

In this question, we will review implementing operations on binary search trees from Data Structures. Balanced binary search trees are common in standard libraries to implement collections, such as sets or maps. For example, the Google Closure library for JavaScript has goog.structs.AvlTree. For simplicity, we will not worry about balancing in this question.

Trees are important structures in developing interpreters, so this question is also critical practice in implementing tree manipulations.

A binary search tree is a binary tree that satisfies an ordering invariant. Let n be any node in a binary search tree whose data value is d, left child is l , and right child is r . The ordering invariant is that all of the data values in the subtree rooted at l must be < d, and all of the data values in the subtree rooted at r must be ≥ d.

We will represent a binary trees containing integer data using the following Scala case classes and case objects:

sealed abstract class SearchTree

case object Empty extends SearchTree

case class Node(l: SearchTree, d: Int, r: SearchTree) extends SearchTree

A SearchTree is either Empty or a Node with left child l, data value d, and right child r.

For this question, we will implement the following four functions.

(a) The function repOk

def repOk(t: SearchTree): Boolean

checks that an instance of SearchTree is valid binary search tree. In other words, it checks using a traversal of the tree the ordering invariant. This function is useful for testing your implementation. A skeleton of this function has been provided for you in the template.

Instructor Solution: 7 lines (including 2 lines for closing braces).

(b) The function insert

def insert(t: SearchTree, n: Int): SearchTree

inserts an integer into the binary search tree. Observe that the return type of insert is a SearchTree. This choice suggests a functional style where we construct and return a new output tree that is the input tree t with the additional integer n as opposed to destructively updating the input tree.

Instructor Solution: 4 lines (including 1 line for a closing brace).

(c) The function deleteMin

def deleteMin(t: SearchTree): (SearchTree, Int)

deletes the smallest data element in the search tree (i.e., the leftmost node). It returns both the updated tree and the data value of the deleted node. This function is intended as a helper function for the delete function. Most of this function is provided in the template.

Instructor Solution: 9 lines (including 2 lines for closing braces and 1 line for a require). (d) The function delete

def delete(t: SearchTree, n: Int): SearchTree

removes the first node with data value equal to n. This function is trickier than insert because what should be done depends on whether the node to be deleted has children or not. We advise that you take advantage of pattern matching to organize the cases.

Instructor Solution: 10 lines (including 2 lines for closing braces).

JavaScripty Interpreter: Numbers.

JavaScript is a complex language and thus difficult to build an interpreter for it all at once. In this course, we will make some simplifications. We consider subsets of JavaScript and incrementally examine more and more complex subsets during the course of the semester. For clarity, let us call the language that we implement in this course JAVASCRIPTY.

For the moment, let us define JAVASCRIPTY to be a proper subset of JavaScript. That is, we may choose to omit complex behavior in JavaScript, but we want any programs that we admit in JAVASCRIPTY to behave in the same way as in JavaScript.

In actuality, there is not one language called JavaScript but a set of closely related languages that may have slightly different semantics. In deciding how a JAVASCRIPTY program should behave, we will consult a reference implementation that we fix to be Google’s V8 JavaScript Engine. We will run V8 via Node.js, and thus, we will often need to write little test JavaScript programs and run it through Node.js to see how the test should behave.

In this lab, we consider an arithmetic sub-language of JavaScript (i.e., an extremely basic calculator). The first thing we have to consider is how to represent a JAVASCRIPTY program as data in Scala, that is, we need to be able to represent a program in our object/source language JAVASCRIPTY as data in our meta/implementation language Scala.

To a JAVASCRIPTY programmer, a JAVASCRIPTY program is a text file—a string of charac-ters. Such a representation is quite cumbersome to work with as a language implementer. Instead, language implementations typically work with trees called abstract syntax trees (ASTs). What strings are considered JAVASCRIPTY programs is called the concrete syntax of JAVASCRIPTY, while the trees (or terms) that are JAVASCRIPTY programs is called the abstract syntax of JAVASCRIPTY. The process of converting a program in concrete syntax (i.e., as a string) to a program in abstract syntax (i.e., as a tree) is called parsing.

For this lab, a parser is provided for you that reads in a JAVASCRIPTY program-as-a-string and converts into an abstract syntax tree. We will represent abstract syntax trees in Scala using case classes and case objects. The correspondence between the concrete syntax and the abstract syntax representation is shown in Figure 1.

sealed abstract class Expr

case class N(n: Double) extends Expr

N(n) n

case class Unary(uop: Uop, e1: Expr) extends Expr Unary(uop, e1) uop e1

case class Binary(bop: Bop, e1: Expr, e2: Expr) extends Expr Binary(bop, e1, e2) e1 bop e2

sealed abstract class Uop

case object Neg extends Uop

Neg −

sealed abstract class Bop

case object Plus extends Bop

Plus +

case object Minus extends Bop

Minus −

case object Times extends Bop

Times ∗

case object Div extends Bop

Div /

Figure 1: Representing in Scala the abstract syntax of JAVASCRIPTY. After each case class or case object, we show the correspondence between the representation and the concrete syntax.

(a)

Interpreter 1. Implement the eval function

def eval(e: Expr): Double

that evaluates a JAVASCRIPTY expression e to the Scala double-precision floating point number corresponding to the value of e.

Consider a JAVASCRIPTY program e; imagine e stands for the concrete syntax or text of the JAVASCRIPTY program. This text is parsed into a JAVASCRIPTY AST e, that is, a Scala value of type Expr. Then, the result of eval is a Scala number of type Double and should match the interpretation of e as a JavaScript expression. These distinctions can be subtle but learning to distinguish between them will go a long way in making sense of programming languages.

At this point, you have implemented your first language interpreter!
