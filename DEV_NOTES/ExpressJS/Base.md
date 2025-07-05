#expressJS 

---

---
Fonction de base:
```js
// Dans le server.js ou index.js

import express from "express";
// Pour pouvoir utiliser cette syntaxe d'import il faut ajouter "type": "module" dans package.json
const app = express();

app.listen(5000, () => {
	console.log("Server started at http://localhost:5000");
})

// Pour lancer le serveur dans le terminal : node chemin/server.js ou nodemon server.js
```

