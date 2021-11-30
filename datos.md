#### Pasos para Instalar SASS y NodeSASS
-----------------------------------
Antes de instalar, verificaremos si tenemos Node.js y NPM instalado.

En la consola de comandos, ejecutamos:

node -v (Si nos tira un número de versión, tenemos instalado Node... no hace falta realizar el Paso 1)
npm -v (Si nos tira un número de versión, tenemos instalado NPM... no hace falta realizar el Paso 2)

1. Instalar Node.js (Ir a https://nodejs.org/es/download/ descargar la versión para Windows 10)
2. Instalar NPM (En la consola de comandos o Terminal de Visual Code, ejecutar: npm install npm@latest -g)
3. Ejecutar npm init (En la consola de comandos o Terminal de Visual Code, ejecutar: npm init ... darle todo ENTER y escribir "yes" al final)
4. Instalar SASS (En la consola de comandos o Terminal de Visual Code, ejecutar: npm install -g sass)
5. Instalar Node-SASS (En la consola de comandos o Terminal de Visual Code, ejecutar: npm install -D node-sass nodemon)
6. Crear la Carpeta "CSS" y dentro de esa carpeta, el archivo "estilos.css"
7. Crear la Carpeta "SCSS" y dentro de esa carpeta, el archivo "estilos.scss"
8. Editar el archivo package.json y agregar estas dos líneas:

"build-css": "node-sass --include-path scss scss/estilos.scss css/estilos.css",
"watch-css": "nodemon -e scss -x \"npm run build-css\""

Guardar el archivo

9. Ejecutar npm run watch-css (En la consola de comandos o Terminal de Visual Code, ejecutar: npm run watch-css)



##### subir cambios a git ####

git add .               //agrega todos los archivos del proyecto modificados agregados o eliminador a la nueva version a enviar por el commit
git commit -m "escribir mensaje de los cambios a subir" // genera el commit con mensaje explicativo
git push origin NOMBRE_DEL_BRANCH //sube los cambios de la pc (local) a la web (remoto)

#### otros comandos de git
chequear estado de version
git status

descargar cambios que pudo hacer otro si comparten el branch
git pull origin NOMBRE_DEL_BRANCH

cambiar de branch
git checkout NOMBRE_DEL_BRANCH

crear nuevo branch
git checkout -b NOMBRE_DEL_BRANCH_NUEVO

### comandos de git cuando trabajas con mas gente

descargar branch nuevos que creo otra persona y subio al remoto
git fetch

traer la ultima version del remoto de este branch, borra todo lo trabajado y no pusheado
git reset b

https://www.atlassian.com/es/git/tutorials/undoing-changes/git-reset




#### Como instalar el ambiente de trabajo en una computadora de 0 

descargar visual studio Code
descargar git bash
descargar nodejs ultima version

despues abrir git bash e ir a la carpeta del proyecto o sea donde queres que este en tu pc almacenado

cd _NOMBRE_DE_RUTA_O_CARPETA /// cd assets esto es para navegar entre carpetas
ejemplos: cd ../  ir para atras cd ./assets ir a la carpeta assets desde donde estoy parado, lo mismo que cd assets

dir // es un comando que muestras los archivos de donde estoy parado
(para diferencias en el listado de dir, archivos de carpetas, es que los archivos tienen extension (.html, .jpg, .etc...)y las carpetas no))

mkdir _nombre_carpeta /// crea una carpeta

rm _nombre_archivo // borra archivo
rm _nombre_carpeta -r // borra la carpeta y todo lo que tiene adentro por el -r de recursivo

#### comandos de npm
npm i | npm install // que instala todas las dependencias de package.json si estas parada donde esta el package.json
npm i -g // instala todo pero de manera global o sea en donde esta instalado nmp ejemplo c:/nodejs/npm

la instalacion de dependencias se guarda en la carpeta node_modules, nunca se sube a versionado

### agregarlo si no esta en .gitignore
gitignore es un archivo medio oculto de git para agregar las rutas de los archivos que no queres versionar

ejemplo node_modules porque pesa un huevo y se actualiza constantemente


### facilidades de uso para visual studio Code
CONTROL + SHIFT + F indenta el codigo, usando la extension prettier
CONTROL + B cierra y abre el side left bar, explorador de archivos de proyecto
CONTROL + SFIT + P comandos de visualcode
CONTROL + P explorador de archivos, podes abrir facilmente un archivo si sabes como se llama
en WIDNDOWS podes cambiar de nombre un archivo tocando F2. Haces click en el archivo y F2 y te selecciona el nombre sin la extension para cambiar
CONTROL + F, seleccionando o no texto te abre el buscador en el documento que estas editando
CONTROL + SHIFT + F, hace lo mismo pero buscando en todos los archivos de tu proyecto
