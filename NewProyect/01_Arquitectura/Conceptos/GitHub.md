
##  **¿Qué es GitHub?**

**GitHub** es una plataforma en línea de desarrollo colaborativo que permite almacenar, gestionar y compartir proyectos de software utilizando [[Git]], un sistema de control de versiones.

> GitHub combina el sistema [[Git ]] con una interfaz web amigable y herramientas para colaborar con otros desarrolladores en proyectos de cualquier tamaño.

---
## **¿Para qué sirve GitHub?**

|        Función         | Descripción                                                                                     |
| :--------------------: | ----------------------------------------------------------------------------------------------- |
|   Almacén de código    | Guarda tu código en la nube ([[Glosario#Repositorio\|repositorio]]).                            |
|  Historial de cambios  | Visualiza todos los cambios hechos en el proyecto.                                              |
|  Trabajo colaborativo  | Permite a múltiples personas trabajar juntas en un mismo [[Glosario#Repositorio\|repositorio]]. |
|  Gestión de versiones  | Controla versiones estables, pruebas y nuevas características.                                  |
|   Revisión de código   | Facilita que otros revisen y comenten tu código (Pull Requests).                                |
| Automatización (CI/CD) | Permite ejecutar tests, despliegues automáticos, etc.                                           |

---
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
