# 🛠️ Guía Maestra de Git: LoboProyect

---

## 1. Configuración de Identidad

_Antes de empezar a trabajar, asegúrate de que Git sepa quién eres._

- **Configurar usuario:** `git config --global user.name "Tu Nombre"`
- **Configurar correo:** `git config --global user.email "tu-correo@ejemplo.com"`
- **Ver nombre configurado:** `git config user.name`
- **Ver correo configurado:** `git config user.email`
- **Ver toda la configuración:** `git config --list`

---

## 2. Inicio y Conexión Remota

_Para crear el repositorio o conectarlo con GitHub por primera vez._

- **Iniciar repo local:** `git init`  
  _(Crea la carpeta oculta `.git` donde se guarda el historial)._
- **Clonar repo existente:** `git clone [url]`  
  _(Descarga un proyecto que ya existe en la nube)._
- **Conectar con GitHub:** `git remote add origin [URL]`  
  _(Crea el "puente" hacia la nube)._
- **Renombrar rama a main:** `git branch -M main`  
  _(Estándar actual de GitHub para la rama principal)._
- **Eliminar Git del proyecto:** `rm -rf .git`  
  _(Borra todo el historial de Git local, úsalo con cuidado)._

---

## 3. Ciclo de Trabajo (El ABC: Staging y Commit)

_Los pasos diarios para registrar tus avances._

- **Ver estado:** `git status`  
  _(Muestra qué archivos han cambiado o no están rastreados)._
- **Añadir un archivo específico:** `git add [archivo]`
- **Añadir TODO al área de preparación:** `git add .`
- **Quitar del staging (Unstage):** `git restore --staged [archivo]`  
  _(Saca el archivo de la "sala de espera" sin borrar tus cambios en el código)._
- **Guardar cambios (Commit):** `git commit -m "[mensaje]"`  
  _(Crea un punto en el historial con un mensaje descriptivo)._
- **Ver diferencias:** `git diff`  
  _(Muestra los cambios antes de hacer el `git add`)._

---

## 4. Sincronización con GitHub (Push y Pull)

_Para enviar y recibir archivos de la nube._

- **Bajar cambios de GitHub:** `git pull origin main`
- **Bajar y unir historias distintas:** `git pull origin main --allow-unrelated-histories`  
  _(Úsalo si el repo de GitHub ya tenía archivos y tu local también)._
- **Subir por primera vez:** `git push -u origin main`  
  _(El `-u` vincula la rama para que luego solo uses `git push`)._
- **Subir cambios normales:** `git push`
- **Descargar sin fusionar:** `git fetch`  
  _(Solo descarga la información para revisar qué hay de nuevo sin tocar tu código)._

---

## 5. Ramas (Branches) y Fusión

_Para trabajar en funciones nuevas sin afectar el código principal._

- **Listar ramas:** `git branch`
- **Crear rama nueva:** `git branch [nombre]`
- **Cambiar de rama:** `git checkout [nombre]`
- **Crear y cambiar rápido:** `git checkout -b [nombre]`
- **Cambiar nombre de la rama actual:** `git branch -m [nuevo-nombre]`
- **Fusionar rama:** `git merge [nombre]`  
  _(Trae los cambios de la rama indicada a tu rama actual)._

---
