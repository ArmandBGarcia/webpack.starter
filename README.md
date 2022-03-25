# Instalacion y Configuracion de Webpack.
####  **Webpack**: Es un empaquetador de modulos, nos ayuda a realizar muchos trabajos de manera automatica por ejemplo:
* Gestionar las dependencias.
* Montar servidores de desarrollo y pruebas: para acelerar el proceso de produccion.
* Cargar modulos: para segmenntar la produccion.
* Convertir a diferentes formatos.
* Minimizar codigo.
* Compilar de SASS a CSS.
* Compilar de TS a JS.
* Nos permite trabajar con JS moderno.

## Pasos a seguir para instalar los archivos iniciales:

1.- Se crea la carpeta del proyecto.

2.- Hacer **npm init** para crear el archivo **package.json** 

Dentro del package.json se creara la configuracion de las dependencias y es primordial para el uso de webpack. Al momento de instalar el package.json se podra ingresar el nombre del paquete y demas datos iniciales de configuracion que se podran cambiar despues.

3.- Es necesario crear una carpeta **src** (source) la cual debe de contener un archivo index.html e index.js. Dentro de la carpeta **src** es recomendable tener una carpeta para puros archivos **Javascript** que luego seran exportados y requeridos por el archivo padre: **index.js**.

4.- Hacer **npm install webpack-cli --save-dev** para instalar la carpeta node modules en la cual iran todos los paquetes que instalemos, adicional a eso se creara el archivo **package-lock.json**

**package-lock.json** sencillamente evita este comportamiento general de actualizar versiones minor o fix de modo que cuando alguien clona nuestro repositorio y ejecuta npm install en su equipo, npm examinará package-lock.json e instalará la versión exacta de los paquete que nosotros habíamos instalado, ignorando así los ^ y ~ de package.json.

El **--save-dev** indica que nuestro webpack es una dependencia de desarrollo. Las dependencias de desarrollo no llegan a la  version de produccion.

5.- Dentro de la carpeta **package.json** en la seccion de **scripts** escribir **"build": "webpack"** despues del webpack se puede poner el nombre de un archivo Javascript, ej: **"build": "webpack --config prod.config.js"** para poder correr el comando **npm run build** el cual creara la carpeta **dist** (distribucion) que dentro tendra el archivo **main.js** el cual contiene todo el codigo de nuestro **index.js** minimizado y ofuscado.

6.- Dentro de **index.html** hacer referencia al archivo **main.js** 

7.- En la raiz del proyecto crear el archivo **webpack.config.js** el cual es el archivo de configuracion para poder utilizar webpack de manera eficiente. Para mas detalles consultar: https://webpack.js.org/configuration/

8.- Dentro de **webpack.config.js** escribir **mode.exports = { mode: 'development', }** para indicar el modo, ya sea production o development.

9.- Dentro de **webpack.config.js** escribir:

**module: {rules: [ ]},**

Dentro iran las reglas que seguiran nuestros modulos.

**optimization: { };**

Dentro iran las optimizaciones

**plugins: [ ],**

Dentro iran los plugins.

10.- Instalar el **html-loader** con **npm install --save-dev html-loader** cargara el archivo hmtl dentro de nuestra carpeta de distribucion. Tambien es necesario instalar el **Html Webpack Plugin** con **npm install --save-dev html-webpack-plugin** el cual ara una injeccion de nuestro archivo hmtl en nuestro index que vamos a terminar generando.

https://webpack.js.org/loaders/html-loader/

https://webpack.js.org/plugins/html-webpack-plugin/

11.-  Me quede en el HTML Loader, continuar despues de ahi.

00.- Instalar babel con **npm install @babel/preset-env --save-dev**

Ir al archivo de configuracion de webpack y configurarlo como inidica en la web, ir seguiendo las indicacion de instalaciones necesarias asi como las configuraciones requeridas.

https://babeljs.io/setup#installation




