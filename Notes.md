- [ ] Section 4: Types in JavaScript 00/12 | 1hr 9min
	- [ ] 54 04-01 0122 Section Overview
	  - All programming languages have Types, that is, the building blocks that allow us to write in that language
	    - Dynamically Typed
	    - Statically Typed
	- [ ] 55 04-02 1340 Javascript Types
	  - 5
		- true
		- 'To be or not to be'
		- undefined
		- null
		- Symbol('just me')
		- {}
		- What about arrays or functions?
		- typeof 5 - 'number'
		- typeof true - 'boolean'
		- typeof 'To be or not to be' - 'string'
		- typeof undefined - 'undefined', the absence of a definition
		- typeof null - 'object', the absence of a value
		  - This is actually a mistake
			- https://twitter.com/BrendanEich/status/1271995509985538048
		- typeof Symbol('just me') - 'symbol'
		- typeof {} - 'object'
		- typeof [] - 'object'
		- typeof function() {} - 'function'; However, arrays and functions are objects

		```javascript
		function a() {
			return 5;
		}

		a.hi = 'Hi';

		console.log(a.hi);
		```

		- What's the difference between the primitive types and the non-primitive types?
		  - Single value, atoms
		- A non-primitive type (variable) doesn't contain actual the value directly.
		  - It has a reference/pointer to the value
			- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects
		- Why do we have things like 'Boolean', 'Number', 'String'? Aren't those primitives?
		- The primitives have "Object Wrappers"

		```javascript
		true.toString() // 'true', the string

		// JavaScript silently provides a wrapper object
		Boolean(true).toString()
		```

		- typeof Math - 'object'
		- typeof Infinity - 'number'
	- [ ] 56 04-03 0217 Array.isArray()	
	- [ ] 57 04-04 1706 Pass By Value vs Pass By Reference
	  - By Value: Copy the value, and create it somewhere else in memory
		- By Reference: Connect to the reference
		- [Lessons on Shallow Cloning and Deep Cloning, including JSON.parse(JSON.stringify(obj))]
	- [ ] 58 04-00 0015 Exercise-Compare Objects
	- [ ] 59 04-00 0003 Exercise-Pass By Reference
	- [ ] 60 04-07 0902 Type Coercion

		```javascript
		// The language converts a certain type to another type
		// All languages have this facility
		1 == '1' 		// true
		1 ==== '1' 	// false
		```

    - https://dorey.github.io/JavaScript-Equality-Table/
		- Object.is, -0, +0
		- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness#:~:text=Strict%20equality%20compares%20two%20values,%2C%20they're%20considered%20equal.
	
	- [ ] 61 04-00 0007 Exercise-Type Coercion
	- [ ] 62 04-00 0011 Quick Note-Upcoming Videos
	- [ ] 63 04-10 1150 JTS-Dynamic vs Static Typing
	  - TypeScript
		- https://stackoverflow.com/questions/2351190/static-dynamic-vs-strong-weak

		```javascript
		var a = 100; // Didn't specify the type (Dynamic Typing)(Type Checking is done during run time)
		int a;
		a = 100; // Type is declared up front (Static Typing)(Type Checking is done during compile time)
		```

		- Pros: With static, self-documenting, less bugs, auto-completion in editors
		- Cons: More code, less simple, why not write better tests? Slower development process
		- TypeScript makes JavaScript behave like a statically-typed language.
	- [ ] 64 04-11 0318 JTS-Weakly vs Strongly Typed

		JavaScript is weakly typed
		```javascript
	  var a = "booooyaa";
		a + 17 // "booooyaa17"
		```

	- [ ] 65 04-12 0945 JTS-Static Typing In JavaScript
	  - flow, reasonML, Elm
		- https://flow.org/
		- https://reasonml.github.io/
		- http://faq.elm-community.org/
		- TypeScript
		- https://insights.stackoverflow.com/survey/2020#technology-most-loved-dreaded-and-wanted-languages-loved