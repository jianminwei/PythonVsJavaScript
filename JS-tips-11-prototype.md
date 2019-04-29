### JavaScript is using prototype inheritance

In JavaScript, a sub-class inherite it's parent properties and methods through "prototype".
Every JS instance has a "__proto__" which pointing to it's parent prototype. For example, every
array instance pointing Array.prototype.

    const arr = [1, 2, 3]

    > arr
    (3) [1, 2, 3]
      0: 1
      1: 2
      2: 3
      length: 3
      __proto__: Array(0)
      
You see arr.__proto__ pointing to Array[0] (prototype)


If you run below function:

    arr.map( e => e * 2)   // will return [2, 4, 6]
    
It's actually doing this behind the scene

    Array.prototype.map.call( [1,2,3], e => e * 2 )
    
arr get the "map" method from Array's prototype. "arr" itself doesn't have "map" method.
But arr is an instance of Array, it traverse up to Array using __proto__ to get the "map" method.
    

    
