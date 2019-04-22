#### Extract a property from an object

    const props = {items:['a','b','c'], name: 'foo'}
    
    > props
    {items: Array(3), name: "foo"}
    
    const f = ({items}) => items;
    
    let my_items = f(props)
    
    > my_items
     ["a", "b", "c"]
     
    
