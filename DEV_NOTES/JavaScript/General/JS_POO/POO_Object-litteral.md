#javascript #poo
___
[[JS_MAP]]
___
Un objet littéral en JavaScript est une syntaxe permettant de créer un objet en utilisant des paires clé-valeur entre accolades `{}`.

```js
const book = {
	title: 'Les fleurs du mal',
	author: 'john doe',
	year: '2020'
	getSummary: function(){
		return `${this.title} est écrit par ${this.author} en ${this.year}`;
	}
};

console.log(book.getSummary()) // Les fleurs du mal est écrit par john doe en 2020
console.log(Object.value(book)) // ["Les felurs du mal", "john doe", "2020"]
console.log(Object.keys(book)) // ["title", "author", "year", "getSummary"]
```
 Voir plus -> [[POO_Constructor]]
 