#javascript #basics 

```js
const data = [
	{
		id: 2,
		title: Les misérables
		author: Victor Hugo
		genres [
			science-fiction,
			aventure,
			action,
			fantastique
		]
	}
]

function getBook(id) {
	return data.find((d) => d.id === id);
}
const book = getBook(2);
// Déstructuration d'objet
const {title, author} = book;

const summary = `${title} est un livre`;
// summary = Les misérables est un livre
```