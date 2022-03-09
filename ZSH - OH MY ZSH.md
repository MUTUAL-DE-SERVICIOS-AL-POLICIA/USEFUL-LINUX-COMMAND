# ZSH y oh-my-zsh

## zsh

**ZSH**, también llamado **Z shell**, es una versión extendida de **Bourne Shell** (**sh**), con muchas características nuevas y soporte para plugins y temas. Se basa en el mismo shell que **Bash**.

Algunas de sus ventajas principales son:
- Eficiencia
- Completado de tabulador mejorado
- Expansión de nombres de fichero mejorada
- Manejo de arrays mejorado
- Totalmente personalizable

### Instalar Zsh
Para instalarlo solo debe ejecutar el siguiente comando:

`sudo apt install zsh`

## Oh-my-zsh
**Oh my zsh** es un distribuidor y administrador de plugins y configuración para **ZSH**, es fácil de instalar y con más de 150 módulos para usar.

### Instalar oh-my-zsh
Para poder instalarlo debe ejecutar el siguiente comando:

`sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`

### Plugins 

####  <ins>Git Plugin</ins>
Este plugin ya viene con **oh-my-zsh**. Proporciona una variedad de ***alias*** y algunas ***funciones*** útiles.

Para usarlo, agregue la palabra ***git*** a la matriz de plugins en el archivo **zshrc**.

`plugins=(git ...)`

##### Ejemplos de uso de alias
Alias | Comando | Descripción
:--: | -- | --
ga | git add | Adiciona un archivo en seguimiento al área *Stage* de Git.
gaa | git add --all | Adiciona todos los archivos en seguimiento al área *Stage* de Git.
gb | git branch | Muestras las ramas creadas.
gcmsg | git commit -m | Realiza la confirmación con un mensaje.
gco | git checkout | Cambiar de rama.
ggl | git pull origin $(rama_actual)| Realiza la extracción del remoto origin configurado, en la rama de trabajo actual.
ggp | git push origin $(rama_actual)| Realiza el empuje del remoto origin configurado, en la rama de trabajo actual.
glo | git log --oneline --decorate | Muestra todas las confirmaciones.
gra | git remote add | Adicionar un repositorio remoto.
grv | git remote -v | Muestra los repositorios remotos configurados.
gst | git status | Muestra el estado del repositorio iniciado.
gss | git status -s | Muestra resumido del estado del repositorio.

Consulte a continuación la [documentación](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git) para mayor información.

#### <ins>Colored-man-pages plugin</ins>
Este plugin también ya se encuentra en el paquete de instalación de **oh-my-zsh**. Nos permite agregar colores de mostrado a las salidas del comando linux ***man***, que es para desplegar documentación de dicho comando.

Para usarlo, agregue la palabra **colored-man-pages** a la matriz de plugins del archivo zshrc.

```zsh
plugins=(
	git
	git-extras
	colored-man.pages
	)
```
Consulte a continuación la [documentación](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/colored-man-pages) para mayor información.

#### <ins>Composer plugin</ins>
Este plugin proporciona alias y facilitación de finalización para comandos frecuentes de *composer*.

Para usarlo, agregue la palabra **composer** a la matriz de plugins en el archivo **zshrc**.

```zsh
	plugins=(
	git
	composer
	...
	)
```
#### Ejemplos de uso de alias
Alias | Comando | Descripción
:--: | -- | --
cpp | composer create-project | Crea un nuevo proyecto a partir de un paquete existente.
ci | composer install | Resuelve e instala dependencias de `composer.json`.
cr | composer require | Agrega nuevos paquetes a `composer.json`
cu | composer update | Actualiza las dependencias y el archivo `composer.lock`

Consulte a continuación la [documentación](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/composer) para mayor información.

#### <ins>Docker Compose plugin</ins>
Este plugin proporciona alias y facilitación de finalización para comandos frecuentes de *docker-compose*.

Para usarlo, agregue la palabra **docker-compose** en la matriz de plugins en el archivo **zshrc**.

```zsh
	plugins=(
	...
	...
	docker-compose
	)
```
##### Ejemplos de uso de alias
Alias | Comando | Descripción
:--: | -- | --
dcb | docker-compose build | Construir contenedores.
dce | docker-compose exec | Ejecutar comando dentro de un contenedor.
dcr | docker-compose run | Ejecutar un comando en el contenedor.
dcstop | docker-compose stop | Detener un contenedor
dcup | docker-compose up | Cree, (re)cree, inicie y adjunte a contenedores para un servicio.
dcdn | docker-compose down | Detener y retirar contenedores.
dcstart | docker-compose start | Iniciar un contenedor

Consulte a continuación la [documentación](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/docker-compose) para mayor información.

#### <ins>Laravel Sail plugin</ins>
##### Instalación

`git clone https://github.com/ariaieboy/laravel-sail ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/laravel-sail`

##### Uso General
Alias | Descripción
:--: | --
s | sail
sup | sail up
sud | sail up -d
sdown | sail down
sb | sail build

##### Comandos Artesan y Dependencias
Alias | Descripción
:--: | --
sa | sail artisan
sp | sail php
sc | sail composer
sn | sail npm

Consulte a continuación la [documentación](https://github.com/ariaieboy/laravel-sail) para mayor información.


#### <ins>zsh-syntax-highlighting  plugin</ins>
Proporciona resalta de color a nuestros comando linux ejecutados en nuestra terminal, bash o zsh. 

Para usarlo, agregue la siguiente palabra **zsh-syntax-hihlighting** en el archivo **zshrc**.

```zsh
	plugins=(...
	...
	zsh-syntax-highlighting
	)
```

#### <ins>zsh-autosuggestions plugin</ins>
Proporcion sugerencia de comandos, a partir de un historial de comandos proporcionados a la terminal. 

Para usarlo, agregue la siguiente palabra **zsh-autosuggestions** en el archivo **zshrc**.

```zsh
	plugins=(...
	...
	zsh-autosuggestions
	)
```

### Actualizando nuestro directorio oh-my-zsh.sh
Para que surja efecto todos los plugins agregados debemos ejecutar el siguiente comando:

`source $ZSH/oh-my-zsh.sh`
...

## Temas oh-my-zsh
También se puede agregar temas de configuración de bash, el más conocido en este caso **powerlevel10k** que se lo puede instalar de la siguiente manera:

`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`

Luego, editamos nuestro archivo **.zshrc**, para configurar el tema.

`vi ~/.zshrc`

En este archivo cambiamos la siguiente línea:

`+  ZSH_THEME="powerlevel10k/powerlevel10k"`

Y por último ejecutamos, el siguiente comando en la terminal, el cuál aparecerá un tipo test para configurar variables de configuración de nuestro bash *zsh* , como ser tipo de codificación, rango de colores soportados, etc.

`p10k configure`


Consulte a continuación la [documentación](https://github.com/romkatv/powerlevel10k) para mayor información.

