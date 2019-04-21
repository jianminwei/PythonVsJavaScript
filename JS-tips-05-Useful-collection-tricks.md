#### map function

    const list = ['aaa', 'bbb', 'ccc']
    
    > list.map( s => s.toUpperCase())
      [ 'AAA', 'BBB', 'CCC' ]
      
    > list.map( (s, i) => console.log(i + ' ' + s) )
      0 aaa
      1 bbb
      2 ccc
