#javascript #basics 

```js
const date = '2025-04-21'

const getYear = (str) => str.split("-")[0];

// A la place de :
	//function getYear(fullDate) {
	//	return fullDate.split("-")[0];
	//}

console.log(getYear(date); // 2025
```