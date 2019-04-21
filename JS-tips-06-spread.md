#### spread a list and an object, the result is different.

    > const list = ['aaa', 'bbb', 'ccc']

    > const recipe = {name: 'Chicken Soup', ingredients: ['chicken','rice','vegies']}

#### spread an object

    > var a = {...recipe}

    > a
    { name: 'Chicken Soup',
      ingredients: [ 'chicken', 'rice', 'vegies' ] }

#### spread a list

    > var b = {...list}

    > b
    { '0': 'aaa', '1': 'bbb', '2': 'ccc' }
    
    It's almost like that a list is just like an object, but the keys are the numeric indexed, 
    vs object the keys are the real property names.
