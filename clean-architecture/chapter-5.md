# Object-oriented programming

## Key points

- Polymorphism existed before OO languages were invented. It is just an application of pointers to functions.
- The main achievement of object-oriented design is that it has made polymorphism much safer and convenient, removing all the manual conventions that the developers had to follow to achieve polymorphism. 
- Polymorphism gives the power to gain control over the source code dependencies, letting separate the system into modules that can be deployed and developed independently, separating the high-level policies from the low-leve details.

## Summary

The basics of a good architecture is the understanding and application of the principles of object-oriented design (OO). But what is OO?

Between different definitions, some people fall back on three words to explain the nature of OO:
- Encapsulation
- Inheritance
- Polymorphism

#### Encapsulation

The author states that encapsulation existed way before OO was even invented (for example, in C we could use header files to declare data structures and functions and then implement them in the implementation files). He also says that some OO languages have weakened encapsulation, and some even have little or no enforced encapsulation, for what it's difficult to accept that OO depends on strong encapsulation.

#### Inheritance

Inheritance is the redeclaration of variables and functions within an enclosing scope, which is something C programmers (and also other languages of that era) were able to do manually long before there was an OO language.

However, the inheritance achieved by C programmers was kind of a trick, but it's not nearly as convenient as true inheritance. Moreover, multiple inheritance is considerably more difficult to achieve by such trickery.

So, it's fair to say that while OO languages did not gave us something completely brand new, it did make the masquerading of data structures sifnificantly more convenient. 

#### Polymorphism

We can achieve polymorphism in languages like C using pointers to functions. You just need to implement a function with the expected signature and then just provide a pointer to that implemented function. This way, you could achieve different behaviours for the same function signature.

This is basis for all polymorphism in OO. 

The most important factor here is that polymorphism is just an application of pointers to functions. Even though it existed before OO languages, they have made polymorphism much safer and convenient. The problem with pointers to functions to create polymorphism is that pointer to functions are dangerous, its use is driven by a set of manual conventions that if the developer forgets to follow, the resulting bug can be very difficult to eliminate. OO eliminates these conventions and, therefore, these dangers, making polymorphism trivial.

And this last point is why we can conclude the statement made in the previous chapter:

```
Object-oriented programming imposes discipline on indirect transfer of control
```

#### Dependency inversion

Before a convenient and safe mechanism for polymorphism was available, in the typical calling tree, main functions called high-level functions, which called mid-level functions, which called low-level functions. In this calling tree, source code dependencies followed the flow of control:

// TODO: add image here

When polymorphism was brought into play, somethign very different can happen

// TODO: add image 2 here

Using an interface, the source code dependency (the inheritance relationship) between `ML1` and the interface `I` points in the opposite direction compared to the flow of control (where `HL1` simply calls `F()` within `ML1`, although indirectly). This is called dependency inversion. The fact that OO languagges provide safe and convenient polymorphism means that any source code dependency, no matter where it is, can be inverted. 

With this approach, software architects working in systems written in OO languages have absolute control iver the direction of all source code dependencies in the system. They are not constraint to allign those dependencies with the flow of control, no matter which module does the calling and which module is called, the software architect can point the source code dependency in either direction. 

What can you do with this `power`? For example, you can rearrange the source code dependencies of your system so that the database and the UI depend on the business rules, rather than the other way around. This means that the business rules never mentions the UI or the database. Changes in the UI and the database have no effect on the business rules. 

#### Conclusion

Copied exactly from the book, I think it adds a lot of value to this chapter:

What is OO? There are many opinions and many answers to this question. To the software architect, however, the answer is clear: OO is the ability, through the use of polymorphism, to gain absolute control over every source code dependency in the system. It allows the architect to create a plugin architecture, in which modules that contain high-level policies are independent of modules that contain low-level details. The low-level details are relegated to plugin modules that can be deployed and developed independently from the modules that contain high-level policies.