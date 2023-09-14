Immutability
Selecting transcript lines in this section will navigate to timestamp in the video
- [Instructor] The first major concept of functional programming is immutability, and it's a concept that may surprise a lot of people at first. Most programmers learned early on that you could assign a value to a variable. For example, we can define a variable called x and store the value five in it. And then, later on in the program, we can change the value of that variable to some completely different number. And later on, we can change this value again, and so on. However, in functional programming, this is not allowed. When we say that x is equal to five, we mean that, for the rest of the program, x will only ever be five. There's no way we can change it. In short, immutability means that most of the values in a program are constant, which, in JavaScript, means using the const keyword instead of the var or let keywords. Another way to think about it is this. In object-oriented and procedural programming, we treat variables as buckets that we can put values into. We call this assigning values to variables. So, at one point in time, x might hold the value three. At another time, it might hold the value 10. At another point, it might be negative four, and so on. On the other hand, in functional programming, we don't assign, we define. Instead of naming buckets that hold different values at different times, we name the values themselves. When we say that x equals three, we don't mean that x is a container that's currently holding the value three, we literally mean that x is three, in the same way that pi is 3.14159 et cetera. Could you imagine changing the value of pi? Of course not. Functional programming treats all values as if they were as concrete and unchanging as pi or any other mathematical constant. And so, once we've defined x, for the whole entire program, x can never be anything else. It's just another name for whatever value we've defined it as. At first glance, this may seem strange to most programmers. After all, what good is a program where you can't change anything? How can a program like that be useful at all? Let's look at a quick example. What if, in a certain theoretical program, we have an employee, and we want to raise their salary? Well, in object-oriented programming, of course, we can just change it directly, usually by calling a member function like this. In functional programming, on the other hand, we would instead define a new constant that represents the updated data and then use this constant in our future calculations. Notice here also that I'm not using the new keyword as we do in object-oriented programming. I'm just defining our data in a JavaScript object. We'll learn more about why this is later on. The advantage of immutability, and the reason that functional programming places such an emphasis on it, is that it frees us from having to deal with state change. When a program contains many variables that are all changing constantly at different times, it can be very hard to know what state a program is in at any given point in time. As programs increase in size to include thousands or even millions of individual variables, this can lead to extremely hard-to-find bugs and an overall fragile code base that programmers are afraid to make changes to. This is a problem that even test-driven development can't solve completely, since the task of testing all possible states that a program might get itself into is nearly impossible in programs of considerable size. In functional programming, on the other hand, we start off with an immutable set of data as a single source of truth, and then we use functions to combine this data piece by piece and transform it into useful information. This data is usually retrieved from a database or some other memory storage. There are two powerful advantages to this approach. The first is that the original data in a program will always remain intact, which makes bugs much easier to find. The second is that programs constructed in this way are much easier to keep track of, since you can focus on any given piece individually. The only thing that determines the output of a given piece is the input. We don't have to think about the entire system all the time. If the concept of immutability doesn't quite make sense to you yet, or if the advantages don't seem apparent, don't worry. Later on in the course, we'll take a look at many examples that incorporate immutability. For now, just remember that in functional programming, all data is immutable, so use const instead of let or var.