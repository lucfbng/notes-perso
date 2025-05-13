#javascript #poo
___
[[JS_MAP]]    |    [[POO_Object-litteral]]    |    [[POO_Constructor]]
___
Un constructeur en JavaScript est une fonction utilisée pour créer et initialiser des objets, généralement définie avec le mot-clé `class` ou `function`.

```js
function Book() {
	console.log('Livre construit');
}
const book1 = new Book(); // Livre construit
```
Le console log marche car la fonction Book() se lance dès qu'on y instancie un objet.

```js
function Book(title, author, year) {
	this.title = title:
	this.author = author;
	this.year = year;
	getSummary: function(){
		return `${this.title} est écrit par ${this.author} en ${this.year}`;
	}
}
const book1 = new Book('Livre1', 'John Doe', '2010');
console.log(book1.getSummary) // Livre1 est écrit par John Doe en 2010
```
`getSummary` fait partie de l'objet ce qui n'est pas forcément une bonne pratique voir -> [[POO_Prototype]]
