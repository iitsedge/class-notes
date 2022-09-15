# Programmer Wisdom

These are some things I've received from others that have had a profound effect on how I write code. Where I remember where I got them from, I'll give attribution. Where I haven't, just assume it wasn't me. ;)

## "Write the Code You Wish You Had"

-- Corey Haines 

```csharp

[HttpPost("/shoppingcart")]
public async Task<ActionResult> ProcessCart([FromBody] Cart request) 
{
// a bunch of validation and stuff here...

// then I have to verify the credit card number...
// "SPOT" - "Single Point of Truth"
var isCreditCardValid = _creditCardValidator.Validate(request.CardInfo);

}

```

## Avoid Premature Abstraction

Don't try to generalize a solution until you thoroughly understand the problem.

Don't go create helper classes, methods, etc. until you know what you need.

:::tip "Never type Private, Always Refactor To it"
- Another one from Corey Haines
::::


## JFHCI - "Just Hard Code It" 
This was advice for Ayende Rahein/Oren Eini 

Deploying software is easy. Don't prematurely build libraries, frameworks, configuration management gools, all that crap until you know you need it.



## Code Duplication Stuff

- "Single Point of Truth" - each piece of business knowledge should exist in exactly one place in an application (Kent Beck)
- "DRY" - "Don't Repeat Yourself"
- "Single Responsibility Principle" - "Each code module should have a single axis of change"
- "Instead of Dry write 'Moist' Code"

## Four Rules of Simple Design

"KISS - Keep It Simple, Smartie!"


[Martin Fowler](https://martinfowler.com/bliki/BeckDesignRules.html)

Originated with Kent Beck.

1. Passes the Tests
    - The code does the right thing. 
2. Reveals Intention
    - How many intentions? One is good.
    - Is this legible? Can a trained programmer look at this and without documentation, grok it, reason through it. Does it show what is intended?
3. No Duplication
    - I don't like "no", 
    - Gross level of duplication is copy and paste
    - Duplication of algorithm, structure, etc.

4. Fewest Number Of Elements
    - Elements are variables, decisions, loops, etc.


## Be Curious - Be Tenacious 



## Naming Things Kent Beck Style

When you are creating an abstraction (a method, a class, etc.) and you aren't sure what to call it, it is because you don't know what it IS yet. Don't give it an "is" until you know what that "is" is. 

Kent Beck says name it using your favorite word of profanity.

Jeff Gonzalez says use a name of a fruit, vegetable, or TACO.

> "If you have a good name for a method, you do not need to look at the body" - Fowler et. al.


## "Strong Opinions Weakly Held"

## Have a Plan but also avoid "Paralysis By Analysis"

- "In order to make an apple pie, you first have to invent the universe" - Carl Sagan

- Don't be afraid to write code that you delete and never see again.



## Simple Vs. Easy

> From Rich Hickey - Creator of the Clojure programming language and other super rad stuff: https://www.infoq.com/presentations/Simple-Made-Easy/

- Simple not the same as Easy
- Easy: "Close at hand"
- Simple from the root word "Simplex"
- Opposite of "Complex" - lots of different things going on. 
    - Lots of different concerns in the same code.



## Joke

There are two hard problems in computer science:

1. Naming Things
2. Cache Invalidation
3. Off By One Errors

