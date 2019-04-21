[This is an example from this link](https://javascript.info/mixins)

The simplest way to make a mixin in JavaScript is to make an object with useful methods, so that we can easily merge them into a prototype of any class.

		// mixin
		let sayHiMixin = {
		  sayHi() {
			alert(`Hello ${this.name}`);
		  },
		  sayBye() {
			alert(`Bye ${this.name}`);
		  }
		};

		// usage:
		class User {
		  constructor(name) {
			this.name = name;
		  }
		}

		// copy the methods
		Object.assign(User.prototype, sayHiMixin);

		// now User can say hi
		new User("Dude").sayHi(); // Hello Dude!
		</script>
