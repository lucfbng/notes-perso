#react #component
___
En React, un composant est une unité modulaire et réutilisable qui représente une partie de l'interface utilisateur. Les composants peuvent être fonctionnels ou basés sur des classes, et ils permettent de structurer l'application en morceaux indépendants et gérables.
(`rfce` raccourci pour créer un composant avec le plugin ES7 React snippet) 

```jsx
import React from 'react'

const name = 'John';
const x = 10;
const y = 20;
const names = ['John', 'Jane', 'Jim', 'Jill'];
const loggedIn = true;
const styles = {
  color: 'blue',
  fontSize: '20px',
  fontWeight: 'bold',
}

const App = () => {
  return (
    <>                                                                         // Un composant ne peut avoir qu'un "parent" qui peut être un fragment (<> </>)
    <h1 className="text-3xl font-bold underline" style = {style}>              // className = "" en React, pas de class = ""
      Hello {name}!                                                            // Hello John
    </h1>
      <p>The sum of {x} and {y} is {x + y}</p>                                 // The sum of 10 and 20 is 30
      <ul>
        {names.map((name, index) => (                                          // Le .map doit obligatoirement avoir une "key", dans ce cas key={index}
          <li key={index}>{name}</li>                                          // John Jane Jim Jill
        ))}
      </ul>
      {loggedIn ? <h1>Welcome back!</h1> : <h1>Please log in</h1>}             // Si loggedIn = true -> Welcome back! sinon -> Please log in
    </>
  )
}

export default App
```
