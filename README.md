# Comandos-de-git
comandos que me sirvieron cuando empece en git 

**1. Configuración Inicial**

- `git init`: Crea un nuevo repositorio Git local en el directorio actual.
- `git clone [url]`: Clona (descarga) un repositorio existente desde una URL remota.
- `git config --global user.name "[nombre]"`: Configura el nombre de usuario para tus commits.
- `git config --global user.email "[email]"`: Configura el correo electrónico para tus commits.

**2. Ciclo de Trabajo Básico (Staging y Commit)**

- `git status`: Muestra el estado de los archivos (modificados, en staging, etc.).
- `git add [archivo]`: Añade un archivo específico al área de preparación (staging).
- `git add .`: Añade todos los cambios del directorio actual al staging.
- `git commit -m "[mensaje]"`: Confirma los cambios preparados, guardándolos en el historial con un mensaje.
- `git diff`: Muestra las diferencias entre archivos no preparados y la última versión.

**3. Ramas (Branches) y Fusión (Merging)**

- `git branch`: Lista las ramas locales.
- `git branch [nombre-rama]`: Crea una nueva rama.
- `git checkout [nombre-rama]`: Cambia a la rama especificada.
- `git checkout -b [nombre-rama]`: Crea una rama y cambia a ella inmediatamente.
- `git merge [nombre-rama]`: Fusiona la rama especificada con la rama actual.
- `git branch -d [nombre-rama]`: Elimina una rama local.

**4. Repositorios Remotos (GitHub, GitLab, Bitbucket)**

- `git remote add origin [url]`: Conecta tu repositorio local con uno remoto.
- `git push -u origin [rama]`: Sube los cambios locales de una rama al repositorio remoto.
- `git pull`: Descarga y fusiona los cambios del repositorio remoto al local.
- `git fetch`: Descarga los cambios del repositorio remoto sin fusionarlos.

**5. Historial y Deshacer**

- `git log`: Muestra el historial de commits.
- `git log --oneline`: Muestra el historial de forma resumida.
- `git reset [archivo]`: Saca un archivo del área de staging, pero conserva los cambios.
- `git revert [commit]`: Crea un nuevo commit que deshace los cambios de un commit anterior.
- `git stash`: Guarda temporalmente los cambios no confirmados para trabajar en otra cosa.
- `git stash pop`: Recupera los cambios guardados con stash.

### Para ver tu configuración actual:

- **Ver el nombre:** `git config user.name`
- **Ver el correo:** `git config user.email`

`git config --list` ver una lista completa de todas tus configuraciones (incluyendo el editor, la rama por defecto, etc.), usa

configuracion de usuario y correo :

- `git config --global user.name "Tu Nombre"`
- `git config --global user.email "tu-correo@ejemplo.com"`

#### Quitarlo de la "sala de espera" (Unstage)

Si solo quieres que NO entre en este commit específico pero que se quede en tu carpeta:

Escribe esto en tu terminal: `git restore --staged desktop.ini`

para subir el repo a git hub 

- **`git remote add origin [URL]`**
Crea el **puente** entre tu computadora y GitHub. Le dice a tu Git local: "esta es la dirección de internet donde quiero subir mi código".
- **`git branch -M main`Renombra** tu rama principal a `main`. Es el estándar actual de GitHub para evitar confusiones con nombres antiguos como `master`.
- **`git pull origin main --allow-unrelated-histories`**
Este fue el "salvavidas". Se usa para **descargar** lo que hay en GitHub y unirlo con lo que tienes en tu PC, incluso si Git piensa que son proyectos diferentes.
- **`git commit -m "mensaje"`**
Es como darle a **"Guardar"** oficialmente. Confirma que los cambios (o la unión de archivos que hicimos) ya están listos y registrados.
- **`git push -u origin main`**
El comando final para **subir** todo. El `u` hace que Git "recuerde" el camino, para que la próxima vez solo tengas que escribir `git push`.
