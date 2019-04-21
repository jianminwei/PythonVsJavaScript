### Python 'dict' vs JS object

	Python:

		>>> type({})
		<class 'dict'>

	JS:
		>typeof({})
		"object"


		
	Python literal:
		>>> {"a":1, "b":2}
		{'a': 1, 'b': 2}	

	JS literal:
		>{a:1, b:2}
		{a: 1, b: 2}	
		
	Python iteration:	
		>>> for i in {"a":1, "b":2}:
		...    print(i)
		...
		a
		b
		
		>>> for i,v in {"a":1, "b":2}.items():
		...    print(i)
		...    print(v)
		...
		a
		1
		b
		2	
		
	JS iteration:
		for(let i in {a:1, b:2}) {
			console.log(i);
		}
		
		a
		b	
		
		Note: JS can't iterate an object using "of"
		
		
		
### Python list vs JS array (object)
	

	Python:
		In [1]: type([])
		Out[1]: list
		
	JS:
		typeof([])
		"object"	
		
	Python literal:
		In [6]: [1,2,3]
		Out[6]: [1, 2, 3]
		
	JS literal:
		>[1,2,3]
		(3) [1, 2, 3]	

	Python iterate:
		In [4]: for i in [1,2,3]:
		   ...:     print(i)
		   ...:
		1
		2
		3	
		
	JS iterate:
		for(let i of [1,2,3]) {
			console.log(i);
		}
		
		1
		2
		3	
		
	Python list comprehension:
		In [5]: [i*i for i in [1,2,3] ]
		Out[5]: [1, 4, 9]

	JS map function:
		[1,2,3].map(x => x*x)
		(3) [1, 4, 9]	


### Python string vs JS string


	Python:
		In [7]: type("")
		Out[7]: str

	JS:
		typeof("")
		"string"


	Python string length:
		In [9]: len("abc")
		Out[9]: 3	
		
	JS string length:
		"abc".length
		3	
		
	Python string iteration:
		In [10]: for c in "abc":
			...:     print(c)
			...:
		a
		b
		c	
		
	JS string iteration:
		for(let c of "abc") {
			console.log(c);
		}
		
		a
		b
		c	

	Python string repeat:
		In [12]: "abc" * 3
		Out[12]: 'abcabcabc'
		
	JS string repeat:
		"abc".repeat(3)
		"abcabcabc"	
		
	Python string startsWith:	
		In [13]: "abc".startswith("ab")
		Out[13]: True
		
	JS string startsWith:
		"abc".startsWith("ab")
		true	
		
