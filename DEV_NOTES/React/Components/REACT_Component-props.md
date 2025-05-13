#react #component #props
___
Les "props" (propriétés) sont des objets qui permettent de passer des données d'un composant parent à un composant enfant. Elles sont immuables et aident à rendre les composants dynamiques et réutilisables.

``
```jsx
// Parent
import Header from './chemin/vers/Header'

const App = () => {
	return (
		<div className = 'container'>
			<Header title = 'Hello'/> // props = props.title = Hello
		</div>
	)
}

export default App
```

```jsx
// Enfant
import PropType from 'prop-type' // Sert a typer les props -> l-20

const Header = (props) => {
// Ou
const Header = ({ title }) => {
	return (
		<header>
			<h1>{props.title}</h1> // Hello
			// Ou
			<h1>{title}</h1>
		</header>
	)
}

// Si aucun title est donné dans le parent il affiche Salut par défaut
Header.defaultProps = {
	title: 'Salut',
}
// Pour le typage des props
Header.propTypes = {
	title: PropType.string, // On peut ajouter .isRequired pour avoir une erreur si aucun prop n'est défini
}


export default App
```

