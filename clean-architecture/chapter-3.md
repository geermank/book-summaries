# Paradigm overview

## Key points


## Summary

#### Structured programming

We can summarize the structured programming as:

```
Structured programming imposes discipline on direct transfer of control (removes go-to statements)
```

#### Object-oriented programming

We can summarize object-oriented programming as:

```
Object-oriented programming imposes discipline on indirect transfer of control (removes function pointers)
```

#### Funtional programming

We can summarize funtional programming as:

```
Funtional programming imposes discipline upon assignment (removes assignment)
```

#### Conclusion

All three paradigms removes capabilities from the programmer and none of them adds new capabilities. The paradigms tell us what not to do, more that they tell us what to do. Since there is nothing left to remove from us, these are the only 3 paradigms that we'll probably see.

What does this have to do with architecture?

Well, everything:

- We use polymorphism to cross architectural boundaries (separation of components)
- We use functional programming to impose discipline on the location of and access to data.
- We use structured programming as the algorithmic foundation of our modules

In the next chapters, these 3 paradigms will be covered more extensively

