#javascript #async
___
Back to [[JS_MAP]]
___
Les callbacks asynchrones sont des fonctions passées en argument à d'autres fonctions pour être exécutées ultérieurement, souvent utilisées pour gérer des opérations non bloquantes comme les requêtes réseau ou les lectures de fichiers.
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

function createPost(post, callback) {
	setTimeout(() => {
		posts.push(post);
		callback();
	}, 2000);
}

createPost({title: 'Post3', body: 'Is post3'}, getPosts);
// Ce qu'il se passe maintenant c'est qu'on attends 2 secondes puis on montre getPosts avec les 3 post dans des <li> 
```
Voir les promesses -> [[Async_Promises]]
