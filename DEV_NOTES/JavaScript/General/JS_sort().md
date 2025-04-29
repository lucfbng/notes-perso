#javascript #methods
___
Back to [[JS_MAP]]
___

La méthode **`sort()`** en JavaScript trie les éléments d'un tableau **dans l'ordre Unicode** par défaut (ce qui peut donner des résultats inattendus pour les nombres).

```js
const nombres = [10, 2, 100];
nombres.sort((a, b) => a - b); // Tri croissant
console.log(nombres); // [2, 10, 100]
```
