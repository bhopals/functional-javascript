## Functional Javascript Concepts

### Functional Programming in simple terms

ROBERT C. MARTIN
> The first rule of the functions is that they should be small. The second rule of the functions is they should be smaller than that.

#### What is functional Programming?, and Why does that matters?
**f(X) = Y**
A function ``f`` that takes ``X`` as its argument and returns the output ``Y``. ``X`` and ``Y`` can be of any number.

 - A function must always takes an argument
 - A function must always return a value
 - A function should act only on its receiving arguments(i.e. X) not the outside world
 - For a given ``X`` there will be only one ``Y``
 
 
 There are 2 more important characteristics of functional programming:
 **- Referential Transparency**
 All the functions are going to return the same value for the same input. With Referential Transparency, we can replace the function with its value, 
 this process is called **Substitution Model**, this leads to **parallel code** and **caching**
 **- Imperative, Declarative, Abstraction**
 Functional Programming is also about being **Declarative** and writing **Abstracted** Code. With Declarative concpets (WHAT to do instead of HOW to do 
 results in **HIGH Order Functions**, as the "HOW" part is being abstracted into common functions.

#### FUNCTIONS v/s METHODS in Javascript

**FUNCTIONS** - A piece of code that can be called by its name. It can pass arguments and return values.
```const simeple = (a) => {return a} // a simple function
   simple(5)                         // called by its name
```
**METHODS** - A piece of code that must be called by its name along with its associate object name.
```const obj = { simple : (a) => {return a} } 
   obj.simple(5) // called by its name along with its associated object 
```

#### Functional Programming Benefits

