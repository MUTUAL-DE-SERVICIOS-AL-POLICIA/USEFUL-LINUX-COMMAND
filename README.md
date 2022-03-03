# USEFUL-LINUX-COMMAND

## **TILIX**
Es un emulador de terminal de mosaico anteriormente conocido como Terminix. Es una mejora con respecto a un terminal normal y proporciona algunas caracteristicas importantes.

**Características**
- Permite dividir terminales tanto en horizontal como vertical.
- Incluye modo Quake-like (la terminal aparece en la parte superior de la pantalla) (--quake)
- Guarda y carga terminales agrupadas

**Instalación**
```
sudo apt update
sudo apt-get install tilix
```

## **NEOFETCH**
Es una herramienta desarrollada en bash que nos permite obtener información básica sobre el sistema instalado.

**Características**
- Posee un archivo de configuración script bash, para personalizar la manera en como se muestra la información del sistema.
- Personalización hasta el último detalle de la información sobre el sistema.
- Posee mas de 50 opciones de configuración.

**Instalación**
```
sudo apt install neofetch
```

## **EXA**
Es el reemplazo moderno del programa de linea de comandos ***ls*** que envia con los sistemas operativos Unix y Linux, con más funciones y mejores incumplimientos.

**Características**
- Uso de colores para mostrar información.
- Muestra los atributos extendidos de un archivo.
- Información del sistema de archivos como el inodo.
- Número de bloques.
- Fechas, horas de creación y modificación de archivos.
- Vista de arbol de los .irectorios (--tree)
 - Ver el estado de Git para un directorio. (también funciona en vista de árbol)

**Instalación Ubuntu**

***Opción 1:***
```
sudo apt install exa
```
***Opción 2:***
```
wget https://github.com/ogham/exa/releases/download/v0.10.1/exa-linux-x86_64-v0.10.1.zip
sudo unzip -q exa-linux-x86_64-v0.10.1.zip bin/exa -d /usr/local
```

## **BAT**
Nos muestra el contenido de un archivo, justo como cat, pero con la sintaxis resaltada para la mayoria de los lenguajes de programación.

**Características**
- Posee resaltado de sintaxis para varios lenguajes de programación.
- Elección de varios temas de colores para dicho resaltado.
- Incluye integración con Git para ver los cambios en el fichero.
- Hace el paginado de forma automática.
- Permite añadir nuevos temas y sintaxis para otros lenguajes no incluidos.

**Instalación**
```
wget https://github.com/sharkdp/bat/releases/download/v0.15.4/bat-musl_0.15.4_amd64.deb
dpkg -i bat-musl_0.15.4_amd64.deb
```
