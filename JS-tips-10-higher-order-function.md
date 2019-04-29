### Higher Order Functions

JavaScript treats functions as any other data types. So you can pass functions as arguments, or return function as result. 
When you pass or return functions. It's called Higher Order Functions. The term comes from mathematics. It's an abstraction 
of operations. When you do imperative programming, you instruct computer to do each steps. When you use Higher Order Function 
, you abstract the operation at higher level.

    A sample data:
    const people = [
        {firstname: "aaFirstName", lastname: "cclastName"},
        {firstname: "ccFirstName", lastname: "aalastName"},
        {firstname:"bbFirstName", lastname:"bblastName"}
    ];

    //define a sortBy function which takes a "property" as argument, and return a comparison function
    const sortBy = (property) => { return (a,b) => (a[property] < b[property]) ? -1 : (a[property] > b[property]) ? 1 : 0; }

    //sort people by "firstname"
    people.sort(sortBy("firstname"))
    
    //output
    0: {firstname: "aaFirstName", lastname: "cclastName"}
    1: {firstname: "bbFirstName", lastname: "bblastName"}
    2: {firstname: "ccFirstName", lastname: "aalastName"}
    
    //sort people by "lastname"
    people.sort(sortBy("lastname"))
    
    //output
    0: {firstname: "ccFirstName", lastname: "aalastName"}
    1: {firstname: "bbFirstName", lastname: "bblastName"}
    2: {firstname: "aaFirstName", lastname: "cclastName"}
