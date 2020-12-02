# Component Oriented Programming

 Summary taken from [https://blog.mediocregopher.com/2020/11/16/component-oriented-programming.html](https://blog.mediocregopher.com/2020/11/16/component-oriented-programming.html)
 
 ## Key Points
 
 - Abstract: A component is an interface consisting of one or more methods
- Instantiatable: An instance of a component, given some set of parameters, can be instantiated as a standalone entity. More than one of the same component can be instantiated, as needed.
 - Composable: A component may be used as a parameter of another component’s instantiation. This would make it a child component of the one being instantiated (the parent).
 - Pure: A component may not use mutable global variables (i.e., singletons) or impure global functions (e.g., system calls). It may only use constants and variables/components given to it during instantiation.
- Ephemeral: A component may have a specific method used to clean up all resources that it’s holding (e.g., network connections, file handles, language-specific lightweight threads, etc.).

## Benefits

### Testing

Its easier to test, there are lots of benifits to writing tests.

### Configuration

AKA [[Dependency-Injection]]

Components are isolated, so easy to either swap out, to configure in different ways, for different use cases.



## Criticisms/Questions

> **Does CoP conflict with object-oriented or functional programming?**
> 
> I don’t think so. OoP languages will have abstract types as part of their core feature-set; most difficulties are going to be with deliberately not using other features of an OoP language, and with imported libraries in the language perhaps making life inconvenient by not following CoP (specifically regarding cleanup and the use of singletons).
