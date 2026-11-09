# 16.1 — Mutable vs Immutable Objects in Java: Advantages, Disadvantages, and Design

> Section 16: Mastering Mutability, Immutability and Final Keyword in Java OOP

Kind: captions Language: en In this section, I want to review the terms mutable and immutable and talk about issues related to these two terms. Objects have state, which is the data stored in instance fields. State can change after an object is created, either intentionally or unintentionally. When state remains constant throughout the lifetime of the object, and code is prevented from changing the state, this object is called an immutable object.

An immutable object is an object whose internal state remains constant. A mutable object is an object whose internal state does not remain constant. Which is better? Well, like anything else, that depends. Working with immutable objects has some advantages. An immutable object isn't subject to unwanted, unplanned and unintended modifications, known as side-effects. This means you don't have to write defensive or protective code for these objects, to protect them from possible mutations.

An immutable class is inherently thread-safe, because no threads at all can change it, once it's been constructed. This allows us to use more efficient collections and operations, which don't have to manage synchronization of access to this object. I'll talk more about this when we get to the threading and synchronization section of the course. These are two of the most important advantages. Working with immutable objects has some disadvantages.

An immutable object can't be modified after it's been created. This means that when a new value is needed, you're probably going to need to make a copy of the object with the new value. Hopefully, you'll remember the discussion comparing String vs. StringBuilder from earlier in the course. If you're constantly needing to alter text values, it's more efficient to use a mutable object like a StringBuilder instance, then generating a lot of new String objects.

I'll be talking about immutable class design coming up. It's important to understand that POJOs and Java Beans, which many code generation tools create, are not by design, immutable, and therefore this architecture may not be the preferred design for your class. This all sounds rather simple, yet there are many topics related to it. One of the most useful tools in our arsenal to build immutable classes, is the final access modifier. I'll be revisiting this modifier in much more detail in the next video, so let's get going.

----------------------------------------
