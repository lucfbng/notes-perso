#javascript  #basics


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
const {title, author} = book; // title = Les misérables author = Victor Hugo
console.log(title) // Les misérables
console.log(author) // Victor Hugo

// Déstructuration de tableau
const [firstGenre, SecondGenre, ...otherGenres] = genres;

console.log(firstGenre) // science-fiction
console.log(secondGenre) // aventure
console.log(otherGenres) // ["action", "fantastique"]

// Ajouter un genre dans un tableau
const newGenres = [...genres, 'fantasy'];
// ['science-fiction', 'aventure', 'action', 'fantastique', 'fantasy']

// On peut ajouter ou ecraser des données
const updatedBook = {
	...book,
	author: 'Moi',
	pages: 567,
}
```