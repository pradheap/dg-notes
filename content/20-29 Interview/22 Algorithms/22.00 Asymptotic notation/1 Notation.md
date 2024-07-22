There are two important things to measure when analyzing an algorithm. One is how long an algorithm takes to complete given its input size? Second is what's the rate of growth for input size?

There are three main notations to measure it and one of them is the commonly used during interviews. Big  Ω (Omega), Big  Θ(Theta) and Big O.

Let's take a look at a simple for loop.
```
for (var guess = 0; guess < array.length; guess++) {
    if (array[guess] === targetValue) { 
        return guess;  // found it!
    }
  }
```
Let `array.length` be `n`.
Each time the for-loop iterates, it has to do several things:
- compare `guess` with `array.length`
- compare `array[guess]` with `targetValue`
- possibly return the value of `guess`
- increment `guess`.
Let's assume the time taken for the above operations is `c1`. We don't know the exact time because it depends on the speed of the computer, the programming language used, the compiler or interpreter that translates the source program into runnable code, and other factors.

This code has a little bit of extra overhead, for setting up the for-loop (including initializing `guess` to 0) and possibly returning `-1` at the end. Let's call the time for this overhead `c2`, which is also a constant. Therefore, the total time for linear search in the worst case is `c1 * n + c2`. But the the constant factor `c1` and the low-order term `c2` don't tell us about the rate of growth of the running time

## Big Theta Θ
Big theta notation is a **asymptotically tight bound** on the running time.
When we say a running time is Θ`(n)`, we say that the running time of the function once it gets past the dashed line, falls in between the upper bound `k2 . n` and lower bound `k1  n` for some constants `k1 and k2`. Here is the pic.
![[big-theta]]
We can use any function, such as n<sup>2</sup> , n log<sub>2</sub>(n) or any other function of n. Here's how to think of a running time that is  Θ`(f(n))` for some function `f(n)`:
For small values of n, we don't care about the running time falling between the upper and lower bounds. 
## Big Omega Ω
Big theta notation is used for **asymptotic lower bound** on the f(n) running time. It means the running time takes at least `k . f(n)`.
![[big-omega]]
## Big O 
Big O notation is used for **asymptotic upper bound** on the f(n) running time. It means the running time is at most `k . f(n)` even for larger inputs.
![[big-O]]
From the reference,
> Because big-O notation gives only an asymptotic upper bound, and not an asymptotically tight bound, we can make statements that at first glance seem incorrect, but are technically correct. For example, it is absolutely correct to say that binary search runs in O(n) time. That's because the running time grows no faster than a constant times n. In fact, it grows slower.

> Think of it this way. Suppose you have 10 dollars in your pocket. You go up to your friend and say, "I have an amount of money in my pocket, and I guarantee that it's no more than one million dollars." Your statement is absolutely true, though not terribly precise.

> One million dollars is an upper bound on 10 dollars, just as O(n) is an upper bound on the running time of binary search. Other, imprecise, upper bounds on binary search would be O(n), O(n<sup>2</sup>), O(n<sup>3</sup>)and O(2<sup>n</sup>). But none of Θ(n), Θ(n<sup>2</sup>), Θ(n<sup>3</sup>)and Θ(2<sup>n</sup>)would be correct to describe the running time of binary search in any case.

References:
https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/big-big-theta-notation