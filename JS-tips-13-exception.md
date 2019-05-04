### Exception handling
  
    class MyError extends Error {
    }

A code block using MyError

    try {
        throw new MyError("bad")
    } catch (e) { 
        if (e instanceof MyError) {
            console.log("caught My error")
        } 
    } finally {
        console.log("in the final block") 
    }
    
