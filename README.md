# BABEL.__GB__
Babel.js es un transcompilador que nos permite convertir nuestro código de JavaScript ES6 en código de ES5


#usage
#Istalacion
Este es babel en si todas las tranformaciones tienen su origen con esta instalacion

```bash
@babel/core
```
para poder usar babel desde consola es con esta instalacion


```bash
@babel/cli
```

para poder usar babel atravez de node
```bash
@babel/node
```
para poder usar las ultimas caracteristicas de babel ya que babel traspila tambien codigo como jsx y posterires debemos instalar este comando

```bash
@babel/preset-env
```
el loader que utilizara webpack para usar babel lo instalamos con
```bash
babel-loader
```
preset para react
```bash
@babel/preset-react 
```
# Para ejecutar la consola con babel
```bash
"scripts":
  "start":"babel-node src/index.js"  //pero para que esto funcione debes poner un archivo .babelrc dentro de tu carpeta master
  "start":"nodemon src/index.js --exec babel-node"  //para ejecutarlo con nodemon y que se mantenga atento a los cambios
```
# .babelrc //este es un archivo necesario para usar babel-node
```bash
{
 "preset": [
        "@babel/preset-env"
  ]
}
```
# para crear el codigo de producion con babel tenemos que crear un scripts para construir ese archivo
  es decir nosotros trabajamos en el archivo de desarrollo y cuando quisieramos tener el archivo de produccion corremos npm run build
  esto nos crea un archivo build con codigo adaptado a emc5 compatible con mas tipos de browsers
```bash
"scripts":
    "build":"babel src --out-dir build"
    
    
    "scripts": {
  
  "build": "babel src --out-dir build", //codigo de produccion
  "dev": "nodemon src/index.js --exec babel-node",//codigo de desarrollo
  "start": "node build/index.js"// ya es el codigo de produccion
  
  },
    ```
