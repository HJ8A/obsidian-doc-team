# 🗄️ ¿Qué es un ORM?

**ORM** significa **Object-Relational Mapping** (Mapeo Objeto-Relacional).

Es una técnica (y también una herramienta) que te permite **interactuar con una base de datos relacional (como MySQL, PostgreSQL o SQLite)** usando **código orientado a objetos**, en lugar de SQL puro.

> 📌 Básicamente, un ORM **traduce objetos en código a tablas de una base de datos** y viceversa.

---

## 🎯 ¿Para qué sirve un ORM?

- Leer y escribir datos en la base de datos sin escribir SQL directamente.
    
- Hacer consultas complejas de forma más intuitiva y segura.
    
- Mantener tu código más limpio y fácil de mantener.
    
- Aplicar migraciones (cambios en la estructura de la base de datos) desde el código.
    

---

## 🧠 ¿Cómo funciona un ORM?

### Ejemplo conceptual

Supón que tienes una tabla llamada `usuarios` con columnas `id`, `nombre` y `email`.

Con un ORM en Node.js (por ejemplo, Sequelize o Prisma), podrías hacer algo así:

// Buscar todos los usuarios
const usuarios = await Usuario.findAll();

// Crear un nuevo usuario
await Usuario.create({ nombre: "Ana", email: "ana@email.com" });


¡Sin escribir ninguna consulta SQL!

---

## 🧰 ORMs populares por lenguaje

| Lenguaje | ORMs populares                       |
| -------- | ------------------------------------ |
| Node.js  | Sequelize, TypeORM, Prisma, MikroORM |
| Python   | SQLAlchemy, Django ORM               |
| PHP      | Eloquent (Laravel), Doctrine         |
| Java     | Hibernate, JPA                       |
| Ruby     | ActiveRecord (Rails)                 |

---

## 🛠️ ORM en Node.js (Ejemplos)

### 🔹 1. **Sequelize**

- Soporta MySQL, PostgreSQL, SQLite y MSSQL.
    
- Sintaxis cercana a SQL.
    
- Muy maduro y documentado.
    

const User = sequelize.define('user', {
  nombre: Sequelize.STRING,
  email: Sequelize.STRING
});


### 🔹 2. **TypeORM** (popular en NestJS)

- Usa decoradores de TypeScript.
    
- Integración natural con NestJS.
    

@Entity()
export class Usuario {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  nombre: string;
}


### 🔹 3. **Prisma**

- Moderno, rápido, enfocado en el desarrollador.
    
- Usa un esquema en archivo `.prisma` para definir la base de datos.
    

model Usuario {
  id     Int     @id @default(autoincrement())
  nombre String
  email  String
}

`const usuarios = await prisma.usuario.findMany();`

---

## ✅ Ventajas de usar un ORM

|Ventaja|Explicación|
|---|---|
|Código más limpio|Menos SQL repetitivo|
|Mayor seguridad|Previene inyecciones SQL|
|Fácil de mantener|Usas modelos en lugar de muchas queries|
|Independencia de base de datos|Más fácil cambiar de MySQL a PostgreSQL, por ejemplo|
|Soporte para migraciones|Evoluciona tu base de datos con el código|

---

## ⚠️ Desventajas de los ORMs

- **Menor rendimiento** en consultas muy complejas (comparado con SQL a mano).
    
- **Abstracción excesiva** puede ocultar problemas si no entiendes bien cómo funciona.
    
- **Curva de aprendizaje** si nunca usaste uno.
    

---

## 🧪 ¿Cuándo usar un ORM?

✅ Usa un ORM si:

- Quieres escribir menos SQL manual.
    
- Tu equipo prefiere trabajar con objetos/clases.
    
- Necesitas mantener y escalar el proyecto fácilmente.
    

❌ Evita el ORM si:

- Necesitas rendimiento ultra preciso y personalizado.
    
- Vas a ejecutar muchas consultas SQL altamente optimizadas.