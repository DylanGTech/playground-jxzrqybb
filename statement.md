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

If you're anywhere near a city, that's pretty fast (so don't tell anyone).
What we just accomplished was using variables that we knew, and an algorithm to calculate a result, which we representated with ANOTHER variable.
Do you see where I'm going going with this yet? (It's ok if you don't, that's why I'll tell you anyway)

## Variables in Machines: A Saving Grace


```C# runnable
// { autofold
using System;

class Hello 
{
    static void Main() 
    {
// }

Console.WriteLine("Hello World!");

// { autofold
    }
}
// }
```
