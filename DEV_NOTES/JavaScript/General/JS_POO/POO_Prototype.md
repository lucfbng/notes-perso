#javascript #poo
___
[[JS_MAP]]
___
Le prototype en JavaScript est un objet à partir duquel d'autres objets héritent de propriétés et de méthodes.

```js
function Book(title, author, year) {
	this.title = title:
	this.author = author;
	this.year = year;
}
// Prototypes
Book.prototype.getSummary = function() {
	return `${this.title} est écrit par ${this.author} en ${this.year}`;
}
Book.prototype.getYears = function() {
	const years = new Date().getFullYear() - this.year;
	return `${this.title} est sortis il y a ${this.years} an(s)`
}
Book.prototype.updateYear = function(newYear) {
	this.year = newYear;
	this.updateYear = true;
}

const book1 = new Book('Livre1', 'John Doe', '2010');
console.log(book1.getSummary()); // Livre1 est écrit par John Doe en 2010
console.log(book1.getYears()); // Livre1 est sortis il y a 25 ans
console.log(book1.updateYear(2000)); // Book {title: "Livre1", author:"John Doe", year:"2000", updateYear: true}
```
Voir d'autres exemples -> [[POO_Object-create]]
Aller plus loin -> [[POO_Héritage]]
