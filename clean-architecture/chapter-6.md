# Functional programming

## Key points



## Summary

In languages like Java, to loop over a list of elements it uses a mutable variable. That variable is the loop control variable, ´i´ in the next example:

´´´
for (int i = 0; i < 25; i++) {
    System.out.println(i*i);
}
´´´

´i´ changes during the execution of the program. On the other hand, in functional languages like Clojure, we don't have a mutable variable to loop a list. Actually, variables are initialized but never modified. Variables in functional languages do not vary.

#### Inmutability and architecture

All the problems we face in concurrent applications (like race conditions) cannot happen in there are no mutable variables. As an architect, you should be very interested in issues of concurrency. You want to make sure that the systems you design will be robust in presence of multiple threads and processors. The question you must be asking yourself, then, is whether immutability is practicable. The answer is yes, if you have infinite storage and processor speed. Lacking those infinite resources, the answer is yes but if certain compromises are made. 

#### Segregation of mutability

One of the most common compromises in regard to inmmutability is to segregate the application, or the services within the application, into mutable and inmmutable components. The inmutable components perform their tasks in a purely functional way, without using any mutable variables. The inmmutable components communicate with one or more other components that are not purely functional, and allow for the state of variables to be mutated. The idea is to push as much processing as possible into the inmmutable components, and to move as much code as possible out of those components that must allow mutation.

#### Event sourcing

Event sourcing is a strategy wherein we store the transactions but not the state. When state is required, we simply apply all the transactions from the beginning of time. An example could be a bank account where we only store the operations made, and when we want the balance we just calculate it from the transactions performed in that account.

In this context, nothing get deleted or updated from the data store. Therefore, there are no concurrent update issues. This of course would require a lot of storage and processing power.

