In Javascript, every iterable object contains a function whose key is Symbol.iterator and this function returns the object iterator.

#### String, Array, Map, Set are all iterable. Note Object is not iterable

    //String
    var iter = "abc"[Symbol.iterator]()
    
    iter.next()
    {value: "a", done: false}
    iter.next()
    {value: "b", done: false}
    iter.next()
    {value: "c", done: false}
    iter.next()
    {value: undefined, done: true}
    
    //Array
    var iter = [10,11][Symbol.iterator]()

    iter.next()
    {value: 10, done: false}
    iter.next()
    {value: 11, done: false}
    iter.next()
    {value: undefined, done: true}
    
    //Set
    const set = new Set().add(1).add(2)

    const iter = set[Symbol.iterator]()
    iter.next()
    {value: 1, done: false}
    iter.next()
    {value: 2, done: false}
    iter.next()
    {value: undefined, done: true}
    
    //Map
    const map = new Map().set(1, "a").set(2, "b")

    const iter = map[Symbol.iterator]()
    iter.next()
    done: falsevalue: (2) [1, "a"]__proto__: Object
    iter.next()
    done: falsevalue: (2) [2, "b"]__proto__: Object
    iter.next()
    {value: undefined, done: true}
