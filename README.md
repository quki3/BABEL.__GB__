# BABEL.__GB__
Babel.js es un transcompilador que nos permite convertir nuestro código de JavaScript ES6 en código de ES5


#usage
#Istalacion
#@babel/core
```bash
Este es babel en si todas las tranformaciones tienen su origen con esta instalacion
```

#@babel/cli
```bash
para poder usar babel desde consola es con esta instalacion
```

#@babel/node
```bash
para poder usar babel atravez de node
```

#@babel/preset-env
```bash
para poder usar las ultimas caracteristicas de babel ya que babel traspila tambien codigo como jsx y posterires debemos instalar este comando
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
    ```
