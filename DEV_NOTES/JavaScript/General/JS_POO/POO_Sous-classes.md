#javascript #poo
___
[[JS_MAP]]
___
Les sous-classes sont des classes qui héritent des propriétés et des méthodes d'une classe parente, permettant ainsi l'extension et la personnalisation du comportement hérité.
```js
class Book {
	constructor(title, author, year) {
		this.title = title;
		this.author = author;
		this.year = year;
	}
	getSummary() {
		return `${this.title} à été écrit par ${this.author} en ${this.year}`;
	}
}
// Sous classe Magazine
class Magazine extends Book {
	constructor(title, author, year, month) {
		super(title, author, year);
		this.month = month;
	}
}
// Instanciation de Magazine
const mag1 = new Magazine('Magazine1', 'John Doe', '2020', 'Janvier');

console.log(mag1.getSummary());
```
