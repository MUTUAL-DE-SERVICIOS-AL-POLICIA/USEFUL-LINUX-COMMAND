# VIM y NEOVIM
## VIM
![VIM logo ](https://www.redeszone.net/app/uploads-redeszone.net/2016/09/Vim-800x388.png)

Para instalar vim utilizamos el siguiente comando

`sudo apt-get install vim`

**Para abrir vim utilizamos el comando** 

`vim`

***si queremos abrir un archivo con vim entramos al archivo de la siguiente forma 
vim <nombre del archivo> 
siempre y cuando se estemos en la ruta donde se encuentra el archivo 
## En vim tenemos varios modos como:

### ***1.- Modo Lector***
 Es el primer modo en el cual nos encontraremos nos servirá solo para visualizar el documento que estamos editando los comandos que podemos utilizar son los siguientes:  

* **h** nos desplazamos hacia la izquierda 
* **j** nos desplazamos hacia abajo
* **k** nos desplazamos hacia arriba abajo
* **l** nos desplazamos hacia la derecha 
(si escribimos primero un número seguido de la dirección a la que nos queremos dirigir (h,j,k,l) desplazar el indicador el numero indicado a la direccion que le iniquemos )  
* **i** entramos en modo editor del archivo 
* **ESC** Para volver al modo lector
* **w** el indicador se desplaza al principio de la siguiente palabra
* **e** el indicador se desplaza al final de la siguiente palabra
* Si mi indicador está una palabra y pongo un **"*"** subrayara donde se encuentra esa palabra repetida 
* **gg** me lleva al principio de todo el documento
* **G** me lleva al final de todo el documento
* **numero+G** me lleva al principio del numero de linea que indique
% me muestra donde se abre o cierra un paréntesis, corchete o llave 
f+<carácter> busca ese carácter en la fila


*** Al entrar al archivo estaremos en modo lector, para poder desplazarnos en el archivo podemos utilizar las flechas pero vim nos da la facilidad de no mover las manos hacia las flechas entonces podemos utilizar las siguientes teclas en el modo lector

### ***2.- Modo Inserción*** 
Podemos acceder a este modo siempre y cuando estemos en el modo lector, podemos entrar a este modo tecleando la letra y esto nos permitirá entrar a escribir el documento donde el indicador se encuentre. Para salir del modo inserción tenemos que apretar la tecla esc

### ***3.- Modo comando***
Para entrar al modo comando necesitaremos escribir dos puntos “:” esto nos permitirá ejecutar algunos comandos como: 
* :q sale del archivo, si no tenemos cambios sin guardar sale sin guardar.

* :q!  sale del archivo descartando los cambios no guardados.

* :w guarda los cambios del archivo, pero no sale de Vim para seguir editando el archivo.

* :wq guarda los cambios y sale de Vim.

### ***4.- Modo visual***

Se utiliza para hacer selecciones de texto del archivo para entrar a este modo entramos con la tecla v
## NEOVIM
![VIM logo ](https://cdn.worldvectorlogo.com/logos/neovim.svg)

Para instalar neovim utilizamos el siguiente comando 

`sudo apt-get install neovim`

En resumen si sabemos utilizar vim es practicamente lo mismo esto porque Neovim es un fork de Vim lo que tenemos que saber es que neovim es el mas actualizado y posee alguna caractericticas nuevas como:

* Nuevo sistema de plugins que permite multitud de nuevos lenguajes: clojure, lisp, go, haskell, lua, javascript, perl, python, ruby y rust

* Nuevas rutas de configuración. El archivo pasa de ~/.vimrc a ~/.config/nvim/init.vim, entre otros. Manteniendo una carpeta de usuario limpia

### Administaradores de plugins en neovim

Lo primero que debemos tener en cuenta es que los archivos que conforman un plugin deben estar en directorios especificos lo que usualmente se hacia en vim y aun se puede hacer en Neovim era pegar estos archivos en su respectivo directorio pero la dificultad viene al tratar de actualizar estos plugins. 

Lo que hace Neovim para solucionar este problema es implementar los administradores de plugins que se encargan de mantener actualizados estos:

algunos de los mas utilizados son:

* pathogen 
* vundle
* dein
* vim-plug 

En este caso instalaremos el vim-plug 

Para instalar vim-plug necesitaremos git y curl 
una vez que tengamos git utilizamos el siguiente comando


`curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim`

Entramos a nuestro archivo 

`nvim ~/.config/nvim/init.vim`

Y agregamos lo siguiente 

```
" Directorio de plugins
call plug#begin('~/.local/share/nvim/plugged')

" Aquí irán los plugins a instalar

call plug#end()

" Luego de esta línea puedes agregar tus configuraciones y mappings

```

Por ejemplo para instalar un pluginde tema para Neovim podemos utilizar el siguiente plugin

*NeoSolarized*
copiamos lo siguiente en nuestro archivo init.vim donde indicamos colocar los plugins

```
Plug 'iCyMind/NeoSolarized'
set termguicolors  " Activa true colors en la terminal
set background=dark  " Fondo del tema: dark/light
colorscheme NeoSolarized  " Activa tema NeoSolarized
```
luego ejecutamos con el modo comando

```
:so ~/.config/nvim/init.vim 
```
luego 
```
:PlugInstall 
```
y cerramos la instalacion con **q**

si vemos nuestro editor nvim tendra la siguiente temas que podemos revisarlos en: 
[Solarized](https://ethanschoonover.com/solarized/ "Título opcional del enlace").




