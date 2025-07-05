#nodejs 



```js
function generateNumber() {

return Math.floor(Math.random() * 100) + 1;

}

module.exports = generateNumber;
```

```js
const generateRandomNumber = require('./utils');
```

