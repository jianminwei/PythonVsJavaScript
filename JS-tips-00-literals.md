#### Javascript literals

    1. Numeric
       
       123
       
       NaN  // Note: NaN is number type, typeof(NaN) return "number"
    
    2. String
    
       'hello'
       
    3. Boolean
    
       true
       false
       
    4. undefined
    
       undefined //Note: undefined is its own type, typeof(undefined) return "undefined"
    
    5. Object
    
       {a: 1, b: "hello", c: [1,2,3]}
       
       null //Note: null is object type, typeof(null) return "object"
       
    6. Array ( Array is a special Object type)
    
       [1, 2, 3]
       
       ['a', 'b', 'c']
       
    7. Set
    
       const set = new Set("abc")  //Note: you have to use "new Set(iterable)" to create a Set. 
                                   //There is no special syntax to start a set literal
                                   
       set.add("d")
       
    7. Map
    
       const m = new Map()  //Note: you have to use "new Map()" to create a Map. 
                                   //There is no special syntax to start a Map literal
                                   
       m.set("a", 1)    
       m.set("b", 2) 
       
    8. Regular expression
     
       /^(\d\d\d\d)-(\d\d)-(\d\d)$/        //Note: reqular expression literal is treated as a special object type

       const [all, year, month, day] =  
       /^(\d\d\d\d)-(\d\d)-(\d\d)$/.exec('2999-12-31');  //note r.exec() return a array
       
    
