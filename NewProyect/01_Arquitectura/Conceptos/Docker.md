## 🐳 ¿Qué es Docker?

**Docker** es una **plataforma de software** que permite crear, probar y ejecutar aplicaciones dentro de **contenedores**.

Un **contenedor** es como una “cajita” que incluye:

- Tu aplicación.
    
- Todo lo que necesita para funcionar (sistema operativo, librerías, dependencias, etc.).
    

Eso significa que puedes ejecutar esa “cajita” en **cualquier máquina**, y funcionará **exactamente igual**, sin importar el sistema operativo o la configuración del equipo.

---

## 🧠 ¿Para qué sirve Docker?

### ✅ Evitar el clásico "¡en mi máquina sí funciona!"

Con Docker, empaquetas todo el entorno de tu aplicación, así no importa dónde lo ejecutes: siempre funcionará igual.

### ✅ Facilita el despliegue

Puedes enviar tu aplicación como un contenedor a servidores, la nube, etc., sin preocuparte por compatibilidad.

### ✅ Automatización y CI/CD

Se usa mucho en procesos de desarrollo continuo, integración y despliegue automático (DevOps).

### ✅ Aislamiento

Cada contenedor es independiente. Puedes tener múltiples aplicaciones o versiones corriendo en el mismo sistema sin que interfieran entre sí.

---

## 🧱 ¿Qué elementos clave tiene Docker?

1. **Dockerfile**: Un archivo donde describes cómo se construye tu contenedor.
    
2. **Imagen (image)**: Una "foto" de tu aplicación ya lista para ejecutarse.
    
3. **Contenedor (container)**: Una instancia en ejecución de una imagen.
    
4. **Docker Hub**: Un repositorio online donde puedes publicar o descargar imágenes listas.
    

---

## 🔧 ¿Cómo funciona?

Ejemplo básico:

1. Escribes un `Dockerfile`:
    

FROM node:18
WORKDIR /app
COPY . .
RUN npm install
CMD ["node", "index.js"]

2. Construyes la imagen:
    

`docker build -t mi-app .`

3. Ejecutas un contenedor:
    

`docker run -p 3000:3000 mi-app`

Y tu app está corriendo en un contenedor, accesible desde tu navegador en `http://localhost:3000`.

---

## 📦 Diferencias entre Máquina Virtual y Docker

|Máquina Virtual|Docker Contenedor|
|---|---|
|Pesa varios GB|Pesa pocos MB|
|Lento en iniciar|Arranca en segundos|
|Tiene su propio SO|Usa el mismo kernel del host|
|Menos eficiente en recursos|Muy eficiente|

---

## 🚀 Casos de uso reales

- Crear entornos de desarrollo consistentes.
    
- Desplegar microservicios.
    
- Ejecutar pruebas automatizadas.
    
- Empaquetar aplicaciones para producción.
    
- Implementar arquitecturas modernas en la nube.