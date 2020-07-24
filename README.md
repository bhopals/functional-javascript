# Functional Javascript Concepts


## 1. Functional Programming in simple terms

ROBERT C. MARTIN
> The first rule of the functions is that they should be small. The second rule of the functions is they should be smaller than that.



### What is functional Programming?, and Why does that matters?

**f(X) = Y**
A function ``f`` that takes ``X`` as its argument and returns the output ``Y``. ``X`` and ``Y`` can be of any number.

 - A function must always takes an argument
 - A function must always return a value
 - A function should act only on its receiving arguments(i.e. X) not the outside world
 - For a given ``X`` there will be only one ``Y``
 
 
 There are 2 more important characteristics of functional programming:

- **&&Referential Transparency**
 All the functions are going to return the same value for the same input. With Referential Transparency, we can replace the function with its value, 
 this process is called **Substitution Model**, this leads to **parallel code** and **caching**

- **Imperative, Declarative, Abstraction**
 Functional Programming is also about being **Declarative** and writing **Abstracted** Code. With Declarative concpets (WHAT to do instead of HOW to do 
 results in **HIGH Order Functions**, as the "HOW" part is being abstracted into common functions.



### FUNCTIONS v/s METHODS in Javascript

**FUNCTIONS** - A piece of code that can be called by its name. It can pass arguments and return values.
```const simple = (a) => {return a} // a simple function
   simple(5)                         // called by its name
```
**METHODS** - A piece of code that must be called by its name along with its associate object name.
```const obj = { simple : (a) => {return a} } 
   obj.simple(5) // called by its name along with its associated object 
```

### Functional Programming Benefits

**Pure Functions**

Pure functions are the functions that return the same output for the given input. Pure functions also should not mutate any external environment variable.

```const double = (value) => value * 2 ```

1. **Pure Functions Lead to Testable Code**

2. **Reasonable Code:** By looking at function name we can easily reason  that this function doubles the result.

3. **Parallel Code:** Pure function allows us to run the code in paralle ( multi threan environment)

4. **Cacheble:** Since the pure function is going to return the same output for the given input, we can cache the function outputs.

5. **Pipelines and Composable:** Pure functions should be designed in such a way that it should do only one thing
> Doing one thing and Doing it perfectly is UNIX Philosophy
We can solve our problem by Composing multiple functions to solve these problems. Thats called **Functional Decomposition**


#### Is Javascript A Functional Programming Language?
And the answer is **YES** and **NO**. This is because as we said in the begining that 
> Functional programming is all about functions which have to take atleast an argument and return a value.

But to be frank, we can create a function in Javascript which takes no argument and infact returns nothing
``` const nope = ()=> {} // still a valid JS function```
And thats the reason Javascript is not a pure functional programming language ( such as LIST, PHYTON, ERLANG, HASKELL) but rather a Multi-paradigm Language. 
However, this langauge is very much sutable. So, in short, Javascript is a language that has support for Functions as arguments, Passing function to
another functions etc - mainly because Javascript treats function as its **first-class-citiznes**


`strict mode` - a restricted varient of javascript





## 2. High-Order Functions

A high-order function is a function that receives the function as its argument and/or return them as outputs.

#### Abstraction and High-Order Function

Generally speaking, high-order functions are written usually to abstract the common problems. In other words, high-order functions are 
nothing but defining abstractions. For instance, `forEach` is an example of abstraction via high-order function. The user of API `forEach` does not 
have to worry about how `forEach` has implemented the traversing part, thus abstracting away the problem.




## 3. Closures and High-Order Functions

#### What are closures?
Simply put Closure is a inner funtion - A function withing another function.

```function outer() {
    function inner() {
    }
}
```

Yes! thats exactly a Closure is. The function `inner` is called a closure function. The reason the Closure is so powerful is because of its access to the 
scope chains ( or scope levels )

**Closure Scopes**

Techincally the Closure has access to three scopes

1. Access to the global variables.
2. Access to the outer function variables.
3. Variable that has declared in its own scope.





