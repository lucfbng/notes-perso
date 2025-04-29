#javascript #methods
___
Back to [[JS_MAP]]
___

La fonction `filter` en JS crée un nouveau tableau contenant uniquement les éléments qui passent un test spécifié par une fonction.

```js
// Exemple (recomandé)
const ages = [22, 10, 54, 1];
const maj = nums.filter(age => age >= 18); // [22, 54]

// Exemple détailé
const maj = nums.filter(function(age) {
	if (age >= 18) {
		return true;
	}
});
```
