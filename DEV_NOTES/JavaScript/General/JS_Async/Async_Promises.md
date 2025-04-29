#javascript #async
___
Back to [[JS_MAP]]
___
Les promesses permettent de gérer les opérations asynchrones en représentant une valeur qui peut être disponible maintenant, à l'avenir ou jamais, avec des méthodes comme `.then()` et `.catch()` pour traiter les résultats ou les erreurs.
```js
const posts = [
{ title: 'Post1', body:'Is post1' },
{ title: 'Post2', body:'Is post2' }
]

function getPosts(){
	setTimeout(() => {
		let output = '';
		posts.forEach((post, index) => {
		});
		document.body.innerHTML = output;
	}, 1000);
}

function createPost(post) {
	return new Promise((resolve, reject) => {
		setTimeout(() => {
			posts.push(post);
			
			const error = false;
			
			if (!error){
				resolve();
			} else {
				reject('Erreur : Nous rencontrons une erreur)
			}
		}, 2000);
	})
}

createPost({title: 'Post3', body: 'Is post3'})
	.then(getPosts); // si error = false il retourne le post
	.catch(err => console.log(err)); // si error = true il affiche "Erreur: Nous rencontrons une erreur"

// Async / Await
async function init() {
	await createPost({title: 'Post3', body: 'Is post3'});
	getPosts();
}
init(); // Il attend la première promesse pour lancer getPosts()

// Async / Await avec Fetch
async function fetchUsers(){
	const response = await fetch('https://jsonplaceholder.typicode.com/users').then(res => res.json());
	const data = await response.json();
	console.log(data);
}
fetchUsers();

// Promose.all
const promise1 = Promise.resolve('RAS');
const promise2 = 10;
const promise3 = new Promise((resolve, reject) => setTimeout(resolve, 2000, 'Goodbye'));
const promise4 = fetch('https://jsonplaceholder.typicode.com/users').then(res => res.json());
Promise.all([promise1, promise2, promise3, promise4]).then(values => console.log(value)); // Affiche un tableau avec les erreurs dedans (["RAS", 10, "Goodbye", Array(10)]) dans ce cas le tableau s'affiche en 2 secondes mais il s'affiche quand les trois promesses ont étés récupérés
```
Retour vers [[Async_Callback]]
