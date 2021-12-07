# C# Tutorial - Part 2: Variables

In the last C# tutorial, we covered the basics of what C# is, and created an extremely simple program (bet you can guess the name of it and what it does) to familiarize you with some of the broad topics we plan to get into in-depth. If you're still brand-stinkin' new to coding, and haven't read that yet, check out Part 1 first!
Today we'll cover where the concept of a variable came from, and how your RAM is literally filled with them.

## Variables in Mathematics: Humble Origins

So believe it or not, you have used variables before if you have taken an algebra course at any point, even as far back as early Middle School (corresponding to late Primary School if you're basically anywhere but the US). That pesky "x" they kept asking you to solve for? Yeah, that's a variable. My schoolteachers hammered into my head the phrase "A variable is any value that can change." Funny enough, in "regular math", that isn't a very good definition. A variable should represents something, and can be any value that makes sense for it.

Here's a good example:
```
given s = d / t
let d = 12 miles (you can use km, if you're one of THOSE people, but I'd be going pretty slow if that was the case)
let t = 1/4 hours
```

Now, you may ask what this all means. This is my drive to work. It takes me 15 minutes to drive 12 miles. There are not one, not two, but THREE variables in this math problem. Each represents something different. "t" is a varuiable that represents the time during my trip, while "d" represents distance travelled during said trip.

What I am doing above is asking myself a question we probably all ask ourselves at least once: "How fast am I going in life?". Thankfully, answering that is quite simple: Divide the distance covered by the time you were measuring.
In my case, I simply substitute all "d" with its value, and "s" with it, and do some long division.
```
s = d / t
s = 12 / (1/4)
s = (12 * 4) / ((1/4) * 4) //Fractions inside of fractions stink, fix it.
s = 48 / 1
s = 48 miles per hour
```

If you're anywhere near the middle of the city, that's kinda fast (so don't tell anyone).

What we just accomplished was using variables that we knew, and an algorithm to calculate a result, which we representated with ANOTHER variable.
Do you see where I'm going going with this yet? (It's ok if you don't, that's why I'll tell you anyway)

## Variables in Machines: A Saving Grace

In the early days of electronic computing, we ran into a problem: Computers were too powerful and too big (100 KiloHertz and 3 Kilobytes was the "gaming computer" of its time, but governments liked to play with them themselves, basically they were the gamers). As more and more people needed to run their highly-advanced calculator homework, they needed a way to simplify how to interact with the computer. Computers store numbers inside their memory as 1s and 0s. The computer does not know what they mean (AI wasn't a thing back then), so programers had to remember what they do, where they are in memory, and what they want the computer to do with them. Doing this with punchcards and tape was extremely difficult. But an old friend from math came to the rescue: Variables.

As mentioned before, variables are relatively simple concept that has been around for a very long time. The process we did above can quite easily translate to a program. Each variable is a piece of computer memory, and the the math we do tells the processor what to do, and where in memory to put them. Programming languages later found inovative ways of handling this. From the days of Formula Translator (FORTRAN) and Common Business-Oriented Language (COBOL), languages have been using variables in some form in order to help the programmer keep track of where things are, so they can focus on solving their problems.

C# uses variables, and was designed from the very beginning to manage the memory as much as possible, so programmers can focus on their code, not the computer running it.

If you remember our code from the last tutorial, it printed "Hello World" to the screen using the Console, and then it stopped.

```C# runnable
using System;

static class Program {
    static void Main()
    {
        Console.WriteLine("Hello World!");
    }
}
```

Today, we will be using the Power of the Computer™ to solve the above problem for us.
Let's begin by adding the variables we know
```C# runnable
using System;

static class Program {
    static void Main()
    {
        var d = 12;
        var t = 15;

        Console.WriteLine("Hello World!");
    }
}
```

So what does this do?
* "var" tells the computer that we need a piece of memory. That piece of memory will be used to store a variable. We did this twice, which means there will be two new pieces of memory to store our data.
* "d" and "t" are the names of the variables. They mean absolutely nothing to the computer. In fact, the computer doesn't even know what the names of those variables are, or what they do, by default. You are like a god to a computer; It will blindly follow your orders, no matter how dumb.
* "d = 12" and "t = 15" tell the computer to take whatever value you give it, and put it inside that piece of memory. After this, the piece of memory with the name "d" will have the value of 15 inside of it, while "t" will have the value of 12.

Now that we have our values neatly tucked away inside their memory slots, it's time to DO something with them.

```C# runnable
using System;

static class Program {
    static void Main()
    {
        var d = 12;
        var t = 0.25;

        var s = d / t;
        Console.WriteLine("Hello World! Your speed is...");
        Console.WriteLine(s);
    }
}
```

We just made some some pretty important changes.
* We created a brand new variable named "s", which we will use to store our speed
* On the same line, we told the computer to take the value "d" and divide it by "t".
* After the computer finished doing the long division, we told the computer to store answer inside "s". We have our answer!
* To let the user know how fast they are going, we tell the Console (represented by the Console class) to write another line with out answer. Try it yourself!

It's important to remember that ALL variables in computing are considered Independant Variables. This means that if you change one value, it does not affect the others unless you specifically tell the computer to later.
If you change the variable later on, the old value is gone, and the other variables stay the same.

Here's what NOT to do:
```C# runnable
using System;

static class Program {
    static void Main()
    {
        var d = 12;
        var t = 0.25;

        d = 16;

        var s = d / t;
        Console.WriteLine("Apparently 12 / 0.25 is...");
        Console.WriteLine(s);
        Console.WriteLine("That doesn't look right.");
    }
}
```
Since the value inside "d" changed from 12 to 16, you get the wrong answer. This is an important thing to keep in mind, and it's a core difference between traditional algebra and computing. Never assume that the variable is going to be the same.

Next lesson, we will go over data types and converting between them. Not all data is created equal!