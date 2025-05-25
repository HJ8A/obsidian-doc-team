# 🟢 ¿Qué es Node.js?

**Node.js** es un **entorno de ejecución para JavaScript** del lado del **servidor**.

> 📌 Permite usar JavaScript fuera del navegador para crear aplicaciones web, APIs, servidores, herramientas de línea de comandos, etc.

Fue construido sobre el motor **V8** de Google Chrome, lo que lo hace **rápido y eficiente**.

---

## 🎯 ¿Para qué sirve Node.js?

- Crear **servidores web**.
    
- Desarrollar **APIs REST o GraphQL**.
    
- Aplicaciones en **tiempo real** (chats, sockets).
    
- Automatizar tareas con herramientas CLI.
    
- Backends para aplicaciones web y móviles.
    

---

## 💡 ¿Por qué usar Node.js?

|Ventaja|Explicación|
|---|---|
|Usa JavaScript en el backend|Un solo lenguaje para cliente y servidor.|
|No bloqueante (non-blocking)|Excelente para apps que manejan muchas conexiones simultáneas.|
|Rápido y eficiente|Gracias a su arquitectura y motor V8.|
|Gran ecosistema (npm)|Miles de librerías disponibles para casi todo.|
|Comunidad enorme|Mucho soporte, ejemplos, y herramientas.|

---

## ⚙️ Cómo funciona Node.js

Node usa un modelo **asíncrono y orientado a eventos**, lo que significa que **no bloquea** la ejecución mientras espera resultados (como acceder a una base de datos o leer un archivo).

### Ejemplo simple:

const fs = require('fs');

fs.readFile('archivo.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log(data);
});

Mientras lee el archivo, el resto del programa sigue funcionando.

---

## 📦 Ecosistema de Node.js

- **npm (Node Package Manager)**: gestor de paquetes.
    
- **Express**: framework web minimalista para crear APIs.
    
- **NestJS**: framework completo y estructurado (basado en Node).
    
- **Socket.io**: para apps en tiempo real.
    
- **Mongoose / Sequelize / Prisma**: para bases de datos.
    

---

## 📁 Estructura típica de un proyecto Node.js

mi-app/
├── node_modules/       # Librerías instaladas
├── package.json        # Configuración del proyecto
├── index.js            # Punto de entrada
└── routes/             # Rutas o endpoints

---

## 🧪 Comandos básicos

# Crear un nuevo proyecto
npm init -y

# Instalar Express
npm install express

# Ejecutar archivo
node index.js


---

## 🚀 Ejemplo: Servidor básico con Express

const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hola desde Node.js');
});

app.listen(3000, () => {
  console.log('Servidor corriendo en http://localhost:3000');
});


---

## 🛠️ Herramientas y extensiones comunes

|Herramienta|Uso principal|
|---|---|
|**Nodemon**|Recarga automática al guardar|
|**dotenv**|Manejo de variables de entorno|
|**Postman**|Probar APIs|
|**Jest / Mocha**|Testing|
|**ESLint / Prettier**|Formato y calidad del código|

---

## ✅ ¿Cuándo usar Node.js?

- Cuando necesitas construir una **API rápida y liviana**.
    
- Para manejar muchas conexiones simultáneas (chats, tiempo real).
    
- Si ya trabajas con **JavaScript** en frontend y quieres usarlo también en backend.