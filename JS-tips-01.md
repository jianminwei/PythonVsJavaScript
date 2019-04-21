### Define short (nick) names for lengthy common functions

      const log = (x) => console.log(x)
      
      const E = React.createElement
      const R = ReactDOM.render
      const ID = (x) => document.getElementById(x)

      R( E('h1', null, 'Hi Jianmin'), ID('content'))

### Block scope

      function f1() {
          log('inside f1');

          function f2() {
              log('function f2() inside f1');
          }

          f2();
      }
      
      
      f1()
      VM210:1 inside f1
      VM210:1 function f2() inside f1
      
      f2()
      VM535:1 Uncaught ReferenceError: f2 is not defined
          at <anonymous>:1:1

### Function Default Parameters

	let today = new Date();

	function makeDate(day, month = today.getMonth(), year = today.getFullYear()) {
		return new Date(year, month, day).toDateString();
	}

	makeDate()
	"Invalid Date"

	makeDate(16)
	"Tue Apr 16 2019"

	makeDate(16,7)
	"Fri Aug 16 2019"

	makeDate(16,7,1999)
	"Mon Aug 16 1999"

### Promise

	const SUCCESS = 1;
	const FAIL = 2;

	//Let's set the status to SUCCESS
	var status = SUCCESS;

	var promise = new Promise(function(resolve, reject) {
	  // the function is executed automatically when the promise is constructed
	  // this logic mimic a real application logic.
	  // it runs 4 seconds, and status is taking from outside for demo purpose
	  if (status == SUCCESS ) {
		 setTimeout(() => resolve("completed"), 4000);
	  } else {
		 setTimeout(() => reject("failed"), 4000);
	  }
	}).then( s => console.log(s))
	  .catch( s => console.log(s));
	
	//.then is executed
	VM14732:14 completed

	//Let's do another test, set the status to FAIL
	status = FAIL;
	
	var promise = new Promise(function(resolve, reject) {
	  // the function is executed automatically when the promise is constructed

	  if (status == SUCCESS ) {
		 setTimeout(() => resolve("completed"), 4000);
	  } else {
		 setTimeout(() => reject("failed"), 4000);
	  }
	}).then( s => console.log(s))
	  .catch( s => console.log(s));
	
	//.catch is executed
	VM14813:10 failed

### Curly braces { } versus parenthesis ( ) in ReactJS

        Curly braces { } are special syntax in JSX. It is used to evaluate a JavaScript expression during compilation. A 
        JavaScript expression can be a variable, function, an object, or any code that resolves into a value.
   
        const yellowStyle={color: 'yellow'} 
        <Star style={yellowStyle} />

        which is same as

        <Star style={{color: 'yellow'}} />

####This is not be confused with Class methods in ES6 which also uses curly braces { }

       class StarsComponent {
           constructor(size) {
           this.size = size;
         }
     
         // Curly braces are used to define a method body in a class
         get size() {
            return this.size;
         }
       }

### How parenthesis ( ) are used?

      Parenthesis are used in an arrow function to return an object.

         () => ({ name: 'Amanda' })  // Shorthand to return an object

      That is equivalent to

         () => {
            return { name : 'Amanda' }
         }


### Parenthesis are used to group multiline of codes on JavaScript returnstatement so to prevent semicolon inserted automatically in the wrong place.

        It is not necessary to add a semicolon in JavaScript. JavaScript engine automatically inserts a 
        semicolon at the first possible opportunity on a line after a return statement. If the JavaScript 
        engine places the semicolon where it should not be, your code won’t compile.

        this doesn’t compile.

        class StarsComponent {
           constructor(size) {
             this.size = size;
           }
  
           render() {
             return <div>  // <--JavaScript engine inserts semicolon here
                *
            </div>
          }
        }


        this works:

        class StarsComponent {
           constructor(size) {
              this.size = size;
           }
  
           render() {
             return (<div> 
               *
             </div>) // <--JavaScript engine inserts semicolon here
           }
       }

       Why? When you place your opening bracket on the same line as return:

       return (
       You are telling JavaScript engine that it can’t automatically insert a semicolon until the bracket is closed.

       return (
         ... 
         ...
      ); <-- inserts semicolon at the end of parenthesis

      For a single line statement, we don’t need to wrap it inside brackets.
