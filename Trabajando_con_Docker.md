# Implantación de aplicaciones web PHP en docker

## Tarea 1 

**Ejecución de la aplicación web PHP bookMedik en docker**

* Queremos ejecutar en un contenedor docker la aplicación web escrita en PHP: bookMedik (https://github.com/evilnapsis/bookmedik).
* Es necesario tener un contenedor con mariadb donde vamos a crear la base de datos y los datos de la aplicación. El script para generar la base de datos y los registros lo encuentras en el repositorio y se llama schema.sql. Debes crear un usuario con su contraseña en la base de datos. La base de datos se llama bookmedik y se crea al ejecutar el script.
* Ejecuta el contenedor mariadb y carga los datos del script schema.sql. Para más información.
* El contenedor mariadb debe tener un volumen para guardar la base de datos.
* Crea una imagen docker con la aplicación desde una imagen base de debian o ubuntu. Ten en cuenta que el fichero de configuración de la base de datos (core\controller\Database.php) lo tienes que configurar utilizando las variables de entorno del contenedor mariadb. (Nota: Para obtener las variables de entorno en PHP usar la función getenv. Para más infomación).
* La imagen la tienes que crear en tu máquina con el comando docker build.
* Crea un contenedor a partir de la imagen anterior, enlazado con el contenedor mariadb, y comprueba que está funcionando (Usuario: admin, contraseña: admin)
* El contenedor que creas debe tener un volumen para guardar los logs de apache2.

## Tarea 2 

**Ejecución de una aplicación web PHP con imagenes de PHP y apache2 de DockerHub**

* Realiza la imagen docker de la aplicación a partir de la imagen oficial PHP que encuentras en docker hub. Lee la documentación de la imagen para configurar una imagen con apache2 y php, además seguramente tengas que instalar alguna extensión de php.
* Crea esta imagen en docker hub.
* Crea un script con docker compose que levante el escenario con los dos contenedores.

## Tarea 3

**Ejecución de un CMS en docker**

* A partir de una imagen base (que no sea una imagen con el CMS), genera una imagen que despliegue un CMS PHP (que no sea wordpress). El contenedor que se crea a partir de esta imagen se tendrá que enlazar con un contenedor mariadb o postgreSQL.
* Crea los volúmenes necesarios para que la información que se guarda sea persistente.

## Tarea 5

**Ejecución de un CMS en docker con una imagen de DockerHub**

* Busca una imagen oficial de un CMS PHP en docker hub (distinto al que has instalado en la tarea anterior, ni wordpress), y crea los contenedores necesarios para servir el CMS, siguiendo la documentación de docker hub.
