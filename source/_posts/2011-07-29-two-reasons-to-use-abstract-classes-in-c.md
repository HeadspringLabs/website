---
layout: post
title: Two Reasons to Use Abstract Classes in C#
categories:
- best practices
- c sharp
- class inheritance
- Developer Deep Dive
- developing with C#
- DRY
status: publish
type: post
published: true
author: logan
---
Do you find yourself writing the same methods over and over in different classes? Say your project needs both a "Dog" class and a "Cat" class -- do you end up writing a "sleep" method for both? What if, in two months, the client needs you to add a "possum" to the system? Do you end up going in and retyping "sleep" instructions yet again? When you're modeling a system with many similar parts, it takes way too much time and effort to keep duplicating code for each class. Imagine how hard it would be to maintain a large project with thousands of classes! Besides, it violates the DRY principle of good programming: Don't Repeat Yourself! There must be a better way.

Thankfully, C# has built-in features for sharing code between classes. One of these is called an "abstract class". Just create a new class with the keyword "abstract" (e.g. "public abstract class Mammal") and write in its body all the methods you would like your other classes to share in common. Since an abstract class is still a class, your "Cat" and "Dog" classes can inherit from it using a colon (e.g. "public Cat : Mammal"). This means that instead of writing a "sleep" method for each animal, you only need to write it in the "Mammal" class, and the other animals will be able to use it too.

But if any class can have inheritance, why not just use a regular class? The answer is that abstract classes have two special features:

1. They cannot be instantiated (made into objects),
1. They can have special methods called "abstract methods".

"Wait a minute," you may be thinking, "Why would I want a class that can't become an object?!" Sounds useless, right? However, consider the purpose of an abstract class: it contains common methods (and fields) that multiple child classes inherit from, but it does not attempt to follow these directions itself. In fact, a parent class is often missing vital information about the methods and fields it contains, because each child may use them a little bit differently. The "Mammal" abstract class only has what is common to all mammals -- since some mammals can't crawl and other mammals can't gallop, the "Mammal" class can't do either one. Imagine what would happen if you tried to instantiate a "generic" mammal: you'd get a featureless mass of hair, muscle and bone that probably wouldn't survive on its own! In the same way, it is undesirable (sometimes dangerous!) to leave a class open to instantiation when it is simply a placeholder for common features. Guard against this possibility by using an abstract class.

What if two classes have methods so different that the only common factor is their name? This is where an abstract method comes in handy. An abstract method looks just like a normal method, except it has the word "abstract" (e.g. "abstract exampleMethod(args);" ) and a semicolon ";" instead of body brackets "{}". What does it do? It basically tells each inheriting class to create its own method with that same name. For instance, since a dog and a bat both sleep, you could write a "sleep" method in the "Mammal" class. However, there are very few commonalities between a dog's sleep and a bat's sleep. So instead of trying to account for each individual animal's sleeping habits, you would make the "sleep" method abstract. Now the code won't even compile until each animal that inherits from "Mammal" has a method called "sleep", using the "override" keyword to replace the abstract one (e.g. "public override sleep(args) {}" ). Now even though all mammals sleep, each individual mammal can sleep in its own way. After this, you may be wondering, "Why even bother putting that method in the parent class? Each inheritor is going to have its own version anyway." You really do want to have that abstract class, not to prevent syntax errors, but to prevent human memory errors. You may know intellectually that all mammals sleep, but without a mechanism forcing you to write a "sleep" method for each mammal, it is all too easy to forget to do so. You may not even realize your mistake until you get a phone call from the client in the middle of the night. By refusing to compile until each abstract method is implemented in every inheriting class, the C# compiler is doing you a favor: it's helping you remember the obvious.

Abstract classes help you improve your code not only through what they can do, but also through what they can't. They can hold common features for many classes to inherit, without accidentally becoming objects themselves. They can also force you to write unique implementations of a common method, preventing human errors of forgetfulness. When you set up a class hierarchy, seriously consider whether you need a normal class to inherit from, or whether an abstract class will do. It may end up making the difference between a solid or buggy program.

Now, if only we had something to write the rest of our code for us...