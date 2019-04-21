#### The idea here is to produce a new object, but keep the the original object immutable

    const person = {name: "Joe", age: 25}

#### The key to create an object clone is to use spread ...

    {...person}

    Here is the output from above in chrome dev tools.
    {name: "joe", age: 25}
      age: 25
      name: "joe"
      __proto__: Object


#### Now to create a clone, but change some properties**

    const person2 = {...person, age: person.age + 1}

    person2
    {name: "joe", age: 26}

#### Another way to create a clone and change some perperties using Object.assign()

    person3 = Object.assign({}, person, {age: person.age + 1})

    {name: "joe", age: 26}

