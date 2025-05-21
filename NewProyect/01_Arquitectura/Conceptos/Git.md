
## **GitHub - Comandos básicos de [[Git]]**

Esta sección contiene los comandos más importantes y utilizados para trabajar con Git y sincronizar con [[GitHub]].

---

##  **Configuración Inicial**

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```
> Crea un nuevo repositorio Git vacío en la carpeta actual.

---

## **Iniciar un [[Glosario#Repositorio | repositorio]]**

```bash
git init
```
> Crea un nuevo repositorio Git vacío en la carpeta actual.
---

## **Clonar un [[Glosario#Repositorio | repositorio]] existente**

```bash
git clone https://github.com/usuario/repositorio.git`
```
> Descarga un repositorio remoto (de GitHub) en tu máquina local.

---

## **Ver estado actual**

```bash
git status
```
> Muestra qué archivos han sido modificados, agregados o eliminados.

---

## **Guardar Cambios (Commit)**

```bash
git commit -m "Mensaje sobre el cambio"
```
> Guarda los cambios agregados con un mensaje descriptivo.

---

## **Enviar cambios al repositorio remoto**

```bash
git push origin main
```
> Sube los commits locales a GitHub (rama principal: `main` o `master`).

---

## **Obtener cambios del repositorio remoto**

```bash
git pull origin main
```
> Enviar cambios al repositorio remoto.

---

## **Ver historial de cambios**

```bash
git log
```
> Muestra la lista de commits realizados en el proyecto.

---

## **Crear y cambiar de rama**

```bash
git branch nueva-rama
git checkout nueva-rama
```
> Crea una nueva rama y permite moverse a ella.

---

## **Fusionar ramas**

```bash
git checkout main
git merge nueva-rama
```
> Combina los cambios de `nueva-rama` con la rama principal.(`IMPORTANTE:`Antes de hacer merge estar ubicado en `main` o `master`).

---

## **Eliminar rama**

```bash
git branch -d nombre-rama
```
> Elimina una rama local que ya no se necesita.

---

## **Conectar Repositorio Local con GitHub**

```bash
git remote add origin https://github.com/usuario/repositorio.git
```
>  Asocia tu repositorio local a uno remoto en GitHub.

---