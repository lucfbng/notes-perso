#javascript #poo
___
[[JS_MAP]]
___
L'héritage permet à une classe de recevoir les propriétés et méthodes d'une autre classe, favorisant ainsi la réutilisation du code et l'organisation hiérarchique.

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

function Magazine(title, author, year, month) {
	Book.call(this, title, author, year);
	this.month = month;
}

// Héritage
Magazine.prototype = Object.create(Book.prototype);

// Instanciation d'un magazine
const mag1 = new Magazine('Magazine1', 'John Doe', '2002', 'Janvier');

// Utiliser le constructeur de Magazine
Magazine.prototype.constructor = Magazine;

console.log(mag1) // {title;'Magazine1', author:'John Doe', year:'2002', month:'Janvier'}
console.log(mag1.getSummary()) // Magazine1 est écrit par John Doe en 2002
```