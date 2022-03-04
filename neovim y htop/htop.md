# HTOP

![VIM logo ](https://blog.trifork.com/wp-content/uploads/2014/08/htop-logo.png)

## ¿QUE ES Y PARA QUE SIRVE?
htop es un sistema de monitorizacion admisnistracion y visualizacion de procesos
## Instalacion
Podemos instalarlo con el siguiente comando 

```
sudo apt-get install htop
```

## Como usar HTOP
una vez que lo tenemos instalado podemos acceder desde la terminal con 

```
htop
```
Y nos mostrara la interfaz de htop de la siguiente forma 

![VIM logo ](https://blog.inovanex.com/wp-content/uploads/2017/12/htop1.jpg)

Donde podemos visualizar 3 areas:

* ***Cabecera:*** Donde podemos observar la cantidad de nucleos y como el proceso esta repartido en ellos, la memoria ram que esta siendo utilizada, el espacio swp, la cantidad de tareas, el tiempo promedio de carga y el tiempo total que la maquina lleva prendida
* ***Tabla de Procesos:*** Donde podemos observar la lista de todos los procesos que estan corriendo con sus respectivos datos
* ***Pie de pagina:*** En esta seccion podemos encontrar las principales funciones de htop

## Funciones de Htop
Como se menciono en la seccion de pie de pagina tenemos las pricipales funciones de htop para acceder a ellas tenemos lo siguiente 

| Teclas            | Funcion     |
|-------------------|-------------|
|F1 o h   | Muestra una página breve de documentación sobre htop que incluye las opciones disponibles y explica el significado de los colores    | 
| F2 o s        | Ayuda a personalizar (configurar) distintas opciones para su htop       | 
| F3 o / | Busca entre los procesos alguno que contenga la palabra indicada |
| F4 o \          | Filtra todos los procesos que contengan la palabra indicada  |
| F5           | Organiza los procesos agrupándolos  |
| F6          | Clasifica los procesos según el parámetro indicado  |   
| F7 o F8          | Sube o baja la prioridad de un proceso, respectivamente |
| F9 o k          | Es una de las características más útiles de htop. Si desea terminar o matar un proceso, simplemente selecciónelo moviendo las flechas y luego presione alguna de estas teclas. Así que no deberá especificar el PID del proceso. |
| F10 o q          | Salir de htop |
| Barra espaceadora          | Etiqueta el proceso, marcándolo en color amarillo |


## Ejemplo
Un ejemplo claro que podriamos realizar es matar el proceso de htop desde htop para ello podemos buscar ese proceso con: 

```
F3 y escribimos htop
```
luego le damos enter e inmediatamente el proceso htop se resaltara una vez que lo veamos nos dirigimos a ese proceso y con F9 lo matamos, confimamos con enter e inmediatamente se cerrara htop. 