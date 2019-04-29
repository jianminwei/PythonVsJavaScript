### What Are Closures?
Simply put closure is an inner function. So what is an inner function? Well, its a function
within an another function. Something like the following:

    function outer() {
        function inner() {
        }
    }
    
Yes, thats exactly what a closure is. The function inner is called a closure function.
The reason why closure is so powerful is because of its access to the scope chains (or
scope levels). 

### Closure remembering Where It Is Born - Closure remembering its context

When inner function is returned, the javascript execution engine sees inner function as a closure and
sets its scope accordingly. Closures will have access to the 3 scope level. All these 3
scope level are set (arg, outer values will be set in scope level of inner function) when the inner 
function is returned! The returned function reference is stored in closureFn. Thus closureFn will have
remember arg, outer values when called via scope chains!

### An example:

    const f1 = (x) => { return () => console.log(x); }
    
f1 is a function that takes a argument, and it returns a function which print out the argument passed.

    let hello = f1('hello');
    
    let hi = f1('hi');
    
    > hello //display hello at the console
    () => console.log(x)
    
     > hi //display hi at the console
    () => console.log(x)   
    
    You see both hello and hi seems the same thing. But when you run it:
    
    hello();
    VM38720:1 hello  //print out hello
    
    hi();
    VM38720:1 hi  //print out hi    

So hello() and hi() remember each one's context (closure).
    
    
    
