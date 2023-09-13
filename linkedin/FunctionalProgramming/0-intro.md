# Module 1 - Intro

## A functional approach to transform code

- [Shaun] An increasing number of developers are switching from object-oriented programming to functional programming as a way to minimize the potential for bugs in their code while maximizing its readability and reusability.
-  Functional programming is an increasingly popular coding paradigm that's been championed by languages like Lisp and Haskell, and its features are natively supported in JavaScript.
-   Writing code using functional programming concepts is the single-most important approach you can take to ensure your applications are maintainable and scalable.
-   In this course, I'll show you how to program in the functional paradigm.
-   We'll start off with the basic concepts of functional programming and how it compares to object-oriented programming, and then move on to first class functions and how to work with them in JavaScript.
-   We'll then move on to seeing how functional programming makes working with data structures very straightforward, followed by some more advanced concepts such as recursion and partial application.
-   Finally, we'll close out with a few interesting challenges that will help you improve your functional knowledge even further.
-    Hi, I'm Shaun Wassell, and I'm a Senior JavaScript and React Developer. Join me in my LinkedIn learning course to learn functional programming with JavaScript ES6 to see how you can take your code to a whole new level.

##  What you should know

- [Instructor] To get the most out of this course, there are few prerequisites that it would be helpful for you to know.
-  The first is a basic knowledge of JavaScript, and ideally some experience with ES6 syntax. If you're not already comfortable with ES6 syntax, it's not hard to learn.
-   If you're interested, I'd recommend checking out one of the ES6 courses in our library. It would also be helpful for you to have some experience with basic command line operations.
-   All we'll be using for this course is basic commands like mkdir to make directories, cd to change directories, and ls to see the contents of a directory, as well as a few commands specific to Node.js.
-    Keep in mind also that if you're on Windows, the commands might be a little different. There are articles out there like this one that show many of the basic Linux commands and their Windows equivalents.
-    And finally, since I'll be using it as a reference point throughout this course, a basic knowledge of object-oriented programming concepts would be helpful to have as well. And even if you're not familiar with object-oriented programming, it's not a big deal.
-     You should still be able to follow along comfortably with the examples.
- While I highly-recommend that you follow along with me as I write the code, I've also included the finished state for all the code that I write in this course in the exercise files for your reference.
- So basically, this course is for low-intermediate to professional developers who have a desire to improve their code by learning and applying functional concepts. If you fit that description, then this course is definitely for you.

## Installing Node.js and npm

- [Instructor] Let's install the tools necessary for this course.
- Node.js will be really important for running your code and installing a few libraries we'll be using to make our programming easy.
-  If you're not already familiar with Node.js, all you need to know for this course is that Node.js is an incredibly popular platform that allows you to run JavaScript code outside of the browser.
-  This is really helpful since it means your JavaScript code doesn't have to be loaded and executed as part of a webpage. In other words, you could write a single JavaScript file and run it from the command line.
-   If you don't already have Node.js installed, you can download it from Node.js's website nodejs.org.
-   We're going to click on this button here and download it and once it downloads we're going to click on it to open it.
-   And this should take you through the steps required for installation. Note that if you're using Windows or a Unix distribution, the steps might be a little different. But Node.js has instructions for all of these as well.
-    And once you have Node.js installed, you'll want to make sure that you have the most recent version of NPM installed.
-    We'll be using a few libraries in this course and NPM is a package manager for Node.js that allows us to easily install them.
-    To install the most recent version of NPM, just open your terminal and type npm install -g npm@latest and you might need to run this with sudo as well.
-    After that, type npm -v and it should show the latest version. If the NPM and Node versions on your computer are higher than mine, don't worry about it.
-    Everything should still run correctly. But I do highly recommend having at least these version numbers here. And that's all there is to it. Node.js and NPM are now installed on your computer.

# Setting up the project

- Before we get into learning functional programming with JavaScript ES6, let's set up an NPM directory that we can use to run our ES6 code.
- Open up a terminal and use cd to navigate to whatever parent directory you want to store the directory for this course in. I'm going to use Documents.
- And then us the make directory command to create a new directory. For example, functional-ES6. And then use cd to move into that directory.
- And once we're inside here, we want to set up our directory as an NPM package.
-  And we'll do that by running NPM init dash y, and the y flag here sets up an NPM package with all the default values.
-   If you want to override the default values for your directory, just leave off the dash y flag.
-   And now that we've set up our directory with NPM, we can install the NPM packages necessary to be able to execute ES6 code with node JS.
-   Currently, node JS doesn't have native support for ES6 syntax, so we need to use a tool called babel to act as the middleman between the modern ES6 syntax that we're going to write, and common JS syntax which node JS can run.
-   This might sound complicated, but it isn't. There are just two steps we need to take in order to get it working. The first thing we need to do is install the necessary bable packages.
-    And we do this by simply running NPM install, dash dash save, at babel slash core, at babel slash node, and at babel slash preset, dash env.
-    And hit enter. And this will run for a little while, but once it finishes, the second thing we need to do is create a new file in our directory.
-    In order to do that, let's open up our directory in an IDE. I'm going to use VSCode here, but feel free to use whatever editor you're comfortable with.
-    So, let's open our directory, mine is in Documents, functional ES6. And inside this directory, we're going to create a new file, and we're going to call it dot babel rc.
-    I'm going to zoom in a little bit here, so that you can see it better.
-    And all we need to do here is create a json object, with a single property called presets.
-    And the value of this property will just be an array with a single string, that says at babel slash preset, dash env.
-    And then we save that file, and that's all we have to do. We shouldn't have to worry about this file ever again for the rest of the course. Now comes the most important part, running our code.
-     From now on, I'm going to be running our code from VSCode's built-in terminal, but you're free to use whatever terminal you want.
- So, normally in node JS, we can run our code by typing node, and then the path to our file, and the file name. So for example, source slash my file dot js.
- But since we're going to be writing our code in ES6 syntax, which isn't yet natively supported by node, the command we're going to use instead is npx babel node, and then the path to our file.


# Setting up the project: Hello World

- [Instructor] Let's create a very simple file. We'll call it hello-world.js, and inside it we'll type some code with very basic ES6 syntax.
- We'll say const sayHello, and that'll be a function that takes our name, and with backticks says hello name. After we've typed this out, let's just call our function with our own name.
- Now, to run our code, make sure you're in the right directory and type npx babel-node, and then hello-world.js, and hit Enter, and we should see the result.
- That's all there is to it. That's how we'll be running all the code in this course.
- It's also worth noting that if you want to play around with this code without writing it in a file first, you can also just type npx babel-node without a file name, and hit Enter,
-  and it'll open up this read a value print loop in our terminal where we can test out different statements.
-  Keep in mind, also, that from now on when I run code in the course I'm going to be running it from the exercise files folder.
-  The only difference that makes is that the file paths in my commands might be a little different, so when you're running your own code just make sure that the file path points to the correct file.


  
