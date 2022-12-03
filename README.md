"# react-vite-hooks-app" 

## Instlaciones test
#### npm i -D jest babel-jest @babel/preset-env @babel/preset-react
#### npm i -D @testing-library/react @types/jest jest-environment-jsdom

### Si ocupas Fetch Api
#### npm i -D whatwg-fetch

## Actualizar los scripts del package.json
````
```
"scripts: {
...
"test": "jest --watchAll"
```
````

## Crear la configuración de babel babel.config.cjs
module.exports = {
presets: [
[ '@babel/preset-env', { targets: { esmodules: true } } ],
[ '@babel/preset-react', { runtime: 'automatic' } ],
],
};
### Opcional, pero eventualmente necesario, crear Jest config y setup:
#### jest.config.cjs
module.exports = {
testEnvironment: 'jest-environment-jsdom',
setupFiles: ['./jest.setup.js']
}
#### jest.setup.js
import 'whatwg-fetch'; // <-- yarn add whatwg-fetch


## PropsType
1- npm i prop-types
2- import PropTypes from 'prop-types'
3- #componente.propTypes = { url: PropTypes.string.isRequired, doAlgo: PropTypes.func.isRequired }

### W -> P para buscar un test en especifico
### u -> actualizar el Snaapshot
### ocupar -> aria-label="form" para que encuentre el elemento