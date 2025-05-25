# 🧑‍💻 ¿Qué es Prisma?

**Prisma** es un **ORM (Object-Relational Mapping)** de nueva generación para **Node.js** y **TypeScript**. Su objetivo es hacer que trabajar con bases de datos SQL (como PostgreSQL, MySQL, SQLite y SQL Server) sea **más fácil, rápido y seguro**.

> 📌 Prisma te ayuda a **leer, escribir y actualizar datos** en la base de datos sin tener que escribir SQL manualmente. Además, proporciona un enfoque basado en **modelos de datos** para estructurar tu base de datos.

---

## 🎯 ¿Para qué sirve Prisma?

- **Interacción con bases de datos**: realiza consultas, inserciones, actualizaciones y eliminaciones de manera sencilla.
    
- **Generación de esquemas**: permite definir los modelos de tu base de datos usando **TypeScript** y genera el código automáticamente.
    
- **Manejo de migraciones**: facilita la creación, ejecución y seguimiento de migraciones en tu base de datos.
    
- **Generación de clientes**: Prisma genera un **cliente de base de datos** que puedes usar en tu aplicación para interactuar con los modelos definidos.
    

---

## 🧱 Componentes principales de Prisma

1. **Prisma Client**: Una API autogenerada para interactuar con la base de datos.
    
2. **Prisma Migrate**: Herramienta de migración de esquemas para modificar tu base de datos de manera controlada.
    
3. **Prisma Studio**: Una interfaz gráfica para interactuar con la base de datos.
    

---

## 🛠️ Instalación y configuración

### 1. Instalar Prisma en tu proyecto

Primero, necesitas inicializar un proyecto Node.js (si no tienes uno):

`npm init -y`

Luego, instala Prisma y su **cliente**:

`npm install prisma @prisma/client`

### 2. Inicializar Prisma

Una vez que Prisma está instalado, necesitas inicializarlo:

`npx prisma init`

Esto creará una carpeta `prisma/` con dos archivos importantes:

- `schema.prisma`: Aquí defines tu **modelo de datos**.
    
- `.env`: Aquí se configura la cadena de conexión a tu base de datos.
    

### 3. Configurar la base de datos

En el archivo `.env`, configura la cadena de conexión a tu base de datos (usando PostgreSQL como ejemplo):

env

CopiarEditar

`DATABASE_URL="postgresql://usuario:contraseña@localhost:5432/mi_base_de_datos?schema=public"`

### 4. Definir el esquema de datos

En el archivo `prisma/schema.prisma`, define los modelos de tu base de datos. Ejemplo:

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

generator client {
  provider = "prisma-client-js"
}

model Usuario {
  id       Int    @id @default(autoincrement())
  nombre   String
  email    String @unique
  edad     Int
}


### 5. Ejecutar migraciones

Para crear la base de datos y las tablas definidas en tu esquema, ejecuta las migraciones:

`npx prisma migrate dev --name init`

Esto creará la base de datos (si no existe) y aplicará las migraciones necesarias.

---

## 💻 Usar Prisma Client en tu código

Una vez configurado todo, puedes usar el **Prisma Client** para interactuar con la base de datos.

### Ejemplo de consultas:

import { PrismaClient } from '@prisma/client';

const prisma = new PrismaClient();

// Crear un nuevo usuario
async function crearUsuario() {
  const usuario = await prisma.usuario.create({
    data: {
      nombre: 'Ana',
      email: 'ana@email.com',
      edad: 30,
    },
  });
  console.log(usuario);
}

// Consultar todos los usuarios
async function obtenerUsuarios() {
  const usuarios = await prisma.usuario.findMany();
  console.log(usuarios);
}

// Actualizar un usuario
async function actualizarUsuario(id: number) {
  const usuarioActualizado = await prisma.usuario.update({
    where: { id },
    data: { edad: 31 },
  });
  console.log(usuarioActualizado);
}

// Eliminar un usuario
async function eliminarUsuario(id: number) {
  const usuarioEliminado = await prisma.usuario.delete({
    where: { id },
  });
  console.log(usuarioEliminado);
}

crearUsuario();
obtenerUsuarios();


---

## 🌟 Características destacadas de Prisma

|Característica|Descripción|
|---|---|
|**Generación automática de cliente**|Prisma genera un cliente altamente optimizado que te permite realizar consultas SQL con un enfoque basado en objetos.|
|**Manejo de migraciones**|Prisma te ayuda a gestionar las migraciones de la base de datos, creando y aplicando cambios de forma controlada.|
|**Tipado fuerte**|Prisma está diseñado para funcionar de manera óptima con **TypeScript**, lo que te da autocompletado, validaciones y control de errores en tiempo de desarrollo.|
|**Prisma Studio**|Una interfaz visual para interactuar con tu base de datos, explorar datos y hacer pruebas sin necesidad de escribir SQL.|

---

## 🧠 Ventajas de usar Prisma

|Ventaja|Explicación|
|---|---|
|**Rápido y eficiente**|Prisma es muy rápido en la ejecución de consultas gracias a su cliente optimizado y consultas preparadas.|
|**Fácil de usar**|La configuración de Prisma es sencilla y su uso es intuitivo, con una excelente integración con **TypeScript**.|
|**Migraciones automáticas**|Prisma facilita el proceso de migración de esquemas, lo que hace que mantener tu base de datos sea mucho más sencillo.|
|**Seguridad**|Prisma ayuda a proteger tu aplicación contra inyecciones SQL mediante un enfoque basado en parámetros.|

---

## ✅ ¿Cuándo usar Prisma?

- Si trabajas con bases de datos SQL (PostgreSQL, MySQL, SQLite, etc.) y prefieres usar un **ORM** eficiente y bien integrado con **TypeScript**.
    
- Si necesitas una **gestión de migraciones** y un **cliente optimizado** para interactuar con tu base de datos.
    
- Si deseas un enfoque más moderno para manejar la base de datos con un **flujo de trabajo de desarrollo eficiente**.