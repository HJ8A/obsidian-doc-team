# 🐘 ¿Qué es PostgreSQL?

**PostgreSQL** (también conocido como **Postgres**) es un **sistema de gestión de bases de datos relacional y de código abierto**. Está diseñado para ser **extensible**, **seguro**, **robusto** y compatible con los estándares SQL.

> 📌 Es una alternativa profesional y gratuita a bases de datos como **MySQL**, **Oracle** o **SQL Server**.

---

## 🎯 ¿Para qué sirve PostgreSQL?

- Almacenar y consultar datos estructurados (relacionales).
    
- Construir sistemas de información, aplicaciones web, sistemas empresariales, APIs, etc.
    
- Ejecutar operaciones complejas sobre grandes cantidades de datos.
    
- Crear relaciones entre tablas con integridad referencial.
    

---

## 💡 ¿Por qué elegir PostgreSQL?

|Ventaja|Descripción|
|---|---|
|🛡️ Robusto y confiable|Muy estable incluso en sistemas complejos|
|🎯 Compatible con SQL|Cumple con el estándar ANSI SQL|
|🧠 Soporte para tipos complejos|Arrays, JSON, XML, UUID, y más|
|🔗 Relaciones y claves|Foreign keys, constraints, índices|
|📦 Soporte para transacciones|ACID completo|
|📈 Escalable|Maneja grandes volúmenes de datos|
|🔌 Extensible|Puedes agregar funciones, tipos y extensiones|

---

## 🧰 Características principales

- **Relacional**: datos organizados en tablas con relaciones entre sí.
    
- **Tipado fuerte**: cada columna tiene un tipo de dato claro.
    
- **Soporte para JSON y NoSQL**: puedes almacenar documentos como en MongoDB.
    
- **Transacciones**: puedes agrupar múltiples acciones como una sola unidad.
    
- **Extensiones**: como PostGIS (para datos geoespaciales), `pg_trgm`, etc.
    
- **Índices avanzados**: B-tree, Hash, GIN, GiST, etc.
    

---

## 🧪 Comandos básicos de PostgreSQL (en SQL)

### Crear base de datos

`CREATE DATABASE mi_base;`

### Crear tabla

CREATE TABLE usuarios (
  id SERIAL PRIMARY KEY,
  nombre VARCHAR(100),
  email VARCHAR(150) UNIQUE,
  edad INT
);

### Insertar datos

`INSERT INTO usuarios (nombre, email, edad) VALUES ('Ana', 'ana@email.com', 25);`

### Consultar datos

`SELECT * FROM usuarios;`

### Actualizar datos

`UPDATE usuarios SET edad = 26 WHERE id = 1;`

### Eliminar datos

`DELETE FROM usuarios WHERE id = 1;`

---

## 🔧 ¿Cómo instalar PostgreSQL?

Puedes instalarlo desde:

- [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
    
- Usar Docker:
    `docker run --name postgres -e POSTGRES_PASSWORD=1234 -p 5432:5432 -d postgres`
    

---

## 📂 Conectarse a PostgreSQL

Puedes conectarte con:

- 🖥️ **pgAdmin** (GUI)
    
- 🧪 **psql** (terminal de PostgreSQL)
    
- 🧑‍💻 **Librerías en código**, como:
    
    - `pg` en Node.js
        
    - `Prisma`, `TypeORM` (ORMs)
        
    - `SQLAlchemy` en Python
        
    - `psycopg2` para scripts Python
        
    - `JDBC` en Java
        

---

## ✅ ¿Cuándo usar PostgreSQL?

- Cuando necesitas **fiabilidad y consistencia** en los datos.
    
- Si vas a trabajar con **relaciones complejas** entre entidades.
    
- Si quieres combinar datos relacionales con estructuras como **JSON**.
    
- Para proyectos empresariales, de gobierno, salud, finanzas, etc.