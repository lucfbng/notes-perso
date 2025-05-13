#javascript #poo
___
Back to [[JS_MAP]]
___

# ES6 Method (better)
Les classes fournissent une syntaxe pour créer des objets et gérer l'héritage, encapsulant ainsi les données et les comportements dans des structures réutilisables.
```js
// Constructor class
class Person {
	constructor(firstName, lastName, dob) {
		this.firstName = firstName;
		this.lastName = lastName;
		this.dob = new Date(dob);
	}
	getBirthYear() {
		return this.dob.getFullYear(); // 1980
	}
	getFullName() {
		return `${this.firstName} ${this.lastName}`; // John Doe
	}
}
const personA = new Person('John', 'Doe', '4-3-1980');
console.log(Person.getBirthYear()); // 1980
```
# Other method (old)

```js
// Constructor function
function Person(firstName, lastName, dob) {
	this.firstName = firstName;
	this.lastName = lastName;
	this.dob = new Date(dob);
}

Person.prototype.getBirthYear = function() {
	return this.dob.getFullYear(); // 1980
}
Person.prototype.getBirthYear = function() {
	return `${this.firstName} ${this.lastName}`; // John Doe
}

// Instanciation d'objet
const personA = new Person('John', 'Doe', '4-3-1980');

console.log(personA);
```

Voir les sous classes -> [[POO_Sous-classes]]
