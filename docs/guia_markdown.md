# Documentacion del uso de mkdocs
* abrimos la consola ejecutamos la siguiente secuencia de ordenes:
    * `sudo apt update  `
    * `sudo apt upgrade ` 
    * `sudo apt install mkdocs`  

Instalamos typora o cualquier editor compatible con markdown (buscar guia en internet)
  
* `mkdocs serve`: Sirve para abrir el servidor local, dara error si falta el archivo mkdocs.yml  
* `mkdocs new my-project`: creamos un nuevo proyecto  
* `cd my-project`: podremos ver el archivo mkdocs.yml  
* `mkdocs serve`: ahora si podremos publicar en local  
* `sudo apt install python3-pip`: segun el SO puede ser necesario instalar el gestor de paquetes de python para instalar los paquetes de mkdocs

Todo lo que hemos echo hasta ahora era en local, a partir de este momento instalaremos lo necesario para hacerlo online.
1. instalamos git, para poder subir nuestros proyectos  
   `sudo apt install git` 
2. configuramos nuestro nombre de usuario  
   `git config --global user.name "Tu Nombre"`
3. configuramos nuestro email  
`git config --global user.email "tu-email@example.com"`
1. Asegurate de generar en GitHub un token, esto te servira mas adelante para identificarte:  
   * Inicia sesión en tu cuenta de GitHub.
   * Ve a Settings (Configuración) desde el menú desplegable en la esquina superior derecha.
   * En el menú de la izquierda, selecciona Developer settings (Configuración de desarrollador).
   * Haz clic en Personal access tokens > Tokens (classic).
   * Haz clic en Generate new token.
   * Asigna un nombre al token, selecciona la duración (por ejemplo, 90 días o sin vencimiento), y asegúrate de darle los siguientes permisos:
     * repo (control total sobre repositorios privados y públicos).
     * workflow (si usas GitHub Actions).
   * Haz clic en Generate token. Copia el token generado. Este es tu "nuevo password" para Git.

2. Antes de seguir asegurate de crearte un repositorio **publico** en tu cuenta de GitHub
3. Inicializa el repositorio Git en tu proyecto  
`git init`
1. Añade los archivosdel directorio actual al repositorio:  
`git add .`
1. Haz un commit inicial:  
`git commit -m "Primer commit"`
1. Conecta tu proyecto a un repositorio GitHub. Si no lo has hecho, crea un nuevo repositorio en GitHub y luego conéctalo usando  
`git remote add origin https://github.com/tu-usuario/tu-repositorio.git`
1.    Sube tus cambios iniciales a GitHub  
`git push -u origin master`
1.    Desplegamos el proyecto  
`mkdocs gh-deploy`