## 🧑‍💻 ¿Qué es GitHub?

**GitHub** es una **plataforma online** que permite **almacenar código**, **colaborar** con otros desarrolladores y **gestionar proyectos** de software. Funciona sobre **Git**, que es un sistema de control de versiones.

> 📌 Piensa en GitHub como una red social para programadores, donde además puedes tener tu portafolio de código.

---

## 🔧 ¿Para qué sirve GitHub?

### ✅ Control de versiones

Puedes ver el historial de cambios de tu código, volver atrás si algo se rompe, o comparar versiones anteriores.

### ✅ Colaboración

Permite que múltiples personas trabajen en un mismo proyecto sin pisarse el trabajo. Ideal para trabajo en equipo.

### ✅ Respaldo

Tu código está guardado en la nube. No se pierde aunque se rompa tu computadora.

### ✅ Gestión de proyectos

Puedes crear tareas, reportar bugs, revisar cambios de otros (pull requests) y más.

### ✅ Despliegue e integración

GitHub se integra con herramientas como Docker, GitHub Actions, Netlify, Vercel, etc., para desplegar apps automáticamente.

---
<<<<<<< HEAD

## 🧩 Elementos clave de GitHub

|Elemento|Descripción|
|---|---|
|**Repositorio (repo)**|El "contenedor" de tu proyecto. Ahí vive tu código, documentación, imágenes, etc.|
|**Commit**|Un "snapshot" de tu código en un momento específico.|
|**Branch (rama)**|Una copia paralela del código para trabajar sin afectar la versión principal (main o master).|
|**Pull Request (PR)**|Una solicitud para fusionar tu trabajo con el de la rama principal. Es donde se revisan y comentan los cambios.|
|**Issues**|Tareas, errores o sugerencias para el proyecto.|
|**Fork**|Una copia de un repositorio que puedes modificar libremente. Ideal para colaborar en proyectos de otros.|

---

## 🧠 ¿Cómo se usa GitHub en el día a día?

1. Crear un repositorio nuevo.
    
2. Clonarlo a tu computadora:
    `git clone https://github.com/usuario/repositorio.git`
    
3. Hacer cambios al código.
    
4. Guardarlos (commit):
    
    `git add .
    `git commit -m "Agrego nueva funcionalidad"`
    
5. Subir los cambios a GitHub:
    `git push origin main`
    

---

## 🛠️ GitHub + Git: ¿Cuál es la diferencia?

|Git|GitHub|
|---|---|
|Sistema de control de versiones local|Plataforma online basada en Git|
|Funciona sin Internet|Requiere estar conectado|
|Lo instalas en tu máquina|Es un servicio web|
|Administra versiones|Administra colaboración|

---

## 🚀 Cosas geniales que puedes hacer en GitHub

- Publicar tu portafolio de proyectos.
    
- Contribuir a proyectos de código abierto.
    
- Automatizar tareas con **GitHub Actions**.
    
- Crear tu sitio web gratis con **GitHub Pages**.
    
- Usar plantillas, proyectos y tableros estilo Kanban.
=======
## **GitHub - Comandos Básicos de Git**
1. Crear una rama nueva después de actualizar el proyecto

2. Hacer merge ( Fusionar los cambios de tu rama local a la rama main )
-Pre requisitos antes de hacer merge
Guardar los cambios en la rama local
```bash
git add .
```
>Prepara todos los archivos de la carpeta


```bash
git commit -m "Estos son mis cambios"
```
>Guarda los cambios de la rama 

#### 2. Cambie a la rama `main`
```bash
git checkout main
```
>Cambiarse a la rama local main

#### 3. Actualice la rama `main` con la versión remota
```bash
git pull origin main
```
>Tener la rama actualizada para evitar conflictos

#### 3. Fusione su rama local con `main`
```bash
git pull origin main
```
>Manda los cambios guardados de una rama  a la rama main

#### 3. Suba la rama `main` fusionada al repositorio remoto
```bash
git push origin main
```
>La rama fusionada en local se sube a la rama remota main
>>>>>>> rama-jisus
