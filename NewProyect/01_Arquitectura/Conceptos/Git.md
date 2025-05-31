
### **GitHub - Comandos básicos de [[Git]]**
Esta sección contiene los comandos más importantes y utilizados para trabajar con Git y sincronizar con [[GitHub]].

## INDICE DE PREGUNTAS


---

###  **Configuración Inicial**

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```
> Crea un nuevo repositorio Git vacío en la carpeta actual.

---

### **Iniciar un [[Glosario#Repositorio | repositorio]]**

```bash
git init
```
> Crea un nuevo repositorio Git vacío en la carpeta actual.

---

### **Clonar un [[Glosario#Repositorio | repositorio]] existente**

```git
git clone https://github.com/usuario/repositorio.git`
```
> Descarga un repositorio remoto (de GitHub) en tu máquina local.

---

### **Ver estado actual**

```git
git status
```
> Muestra qué archivos han sido modificados, agregados o eliminados.

---

### **Guardar Cambios (Commit)**

```git
git commit -m "Mensaje sobre el cambio"
```
> Guarda los cambios agregados con un mensaje descriptivo.

---

### **Enviar cambios al repositorio remoto**

```git
git push origin main
```
> Sube los commits locales a GitHub (rama principal: `main` o `master`).

---

### **Obtener cambios del repositorio remoto**

```git
git pull origin main
```
> Enviar cambios al repositorio remoto.

---

### **Ver historial de cambios**

```git
git log
```
> Muestra la lista de commits realizados en el proyecto.

---

### **Crear una rama local**

```git
git branch nueva-rama
```
> Crea una nueva rama solo visible en la computadora

---

### **Subir una rama local al repositorio remoto**

```git
git push -u origin nueva-rama
```
>Publica la rama local hacia el proyecto remoto. (visible para todos)

---

### **Fusionar ramas**

```git
git checkout main
git merge nueva-rama
```
> Combina los cambios de `nueva-rama` con la rama principal.(`IMPORTANTE:`Antes de hacer merge estar ubicado en `main` o `master`).

---

### **Eliminar rama local**

```git
git branch -d nombre-rama
```
> Elimina una rama guardada solo en tu equipo. (se elimina solo para ti)

---

### **Eliminar rama remota**

```git
git push origin --delete nombre-rama
```
> Elimina una rama guardada en el repositorio remoto. (se elimina para todos)

---

### **Conectar Repositorio Local con GitHub**

```git
git remote add origin https://github.com/usuario/repositorio.git
```
>  Asocia tu repositorio local a uno remoto en GitHub.

---