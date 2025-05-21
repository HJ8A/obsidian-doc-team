# 🚀 ¿Qué es NestJS?

**NestJS** es un **framework para Node.js** que permite construir aplicaciones del lado del servidor (back-end) utilizando **TypeScript** (aunque también soporta JavaScript).

> 🧱 Está inspirado en frameworks como **Angular**, por eso usa conceptos como **módulos**, **controladores** y **servicios**.

---

## 🎯 ¿Para qué sirve NestJS?

NestJS es ideal para construir:

- APIs RESTful o GraphQL
    
- Aplicaciones monolíticas o microservicios
    
- Backends robustos, modulares y fáciles de mantener
    

---

## 🧠 Características clave

|Característica|Explicación|
|---|---|
|**Basado en TypeScript**|Tiene tipado fuerte y herramientas modernas.|
|**Modular**|Puedes dividir tu app en módulos reutilizables.|
|**Soporte para MVC**|Usa controladores, servicios y modelos.|
|**Compatible con Express**|Usa Express (o Fastify) como servidor HTTP.|
|**Inyección de dependencias**|Permite separar lógica de negocio y facilita las pruebas.|
|**Soporta WebSockets y GraphQL**|Para construir APIs en tiempo real o GraphQL nativamente.|
|**Microservicios y eventos**|Tiene herramientas listas para arquitecturas distribuidas.|

---

## 📦 Estructura básica de una app NestJS

src/
├── app.controller.ts      # Controlador (maneja las rutas HTTP)
├── app.service.ts         # Servicio (lógica de negocio)
├── app.module.ts          # Módulo raíz
├── main.ts                # Punto de entrada


---

## 🔧 Comandos básicos (CLI)

Primero, instala el CLI de Nest:

`npm i -g @nestjs/cli`

### Crear un nuevo proyecto:

`nest new mi-proyecto`

### Crear un módulo:

`nest generate module usuarios`

### Crear un controlador:

nest generate controller usuarios`

### Crear un servicio:

`nest generate service usuarios`

---

## 💡 Ejemplo rápido: API de usuarios

### `usuarios.controller.ts`

@Controller('usuarios')
export class UsuariosController {
  constructor(private readonly usuariosService: UsuariosService) {}

  @Get()
  findAll() {
    return this.usuariosService.getUsuarios();
  }
}


### `usuarios.service.ts`

@Injectable()
export class UsuariosService {
  getUsuarios() {
    return [{ id: 1, nombre: 'Ana' }, { id: 2, nombre: 'Luis' }];
  }
}


---

## 🌐 NestJS + REST + Swagger + JWT

NestJS se integra muy fácilmente con:

- **Swagger**: Documentación automática para tu API.
    
- **JWT**: Para autenticación segura.
    
- **TypeORM / Prisma / Mongoose**: Para conectarse a bases de datos SQL o NoSQL.
    

---

## ✅ ¿Cuándo usar NestJS?

- Cuando quieres una arquitectura **limpia y escalable**.
    
- Si vienes de Angular y te gusta su estilo.
    
- Cuando necesitas crear un backend robusto con buenas prácticas desde el inicio.
    
- Para proyectos **enterprise** o backend de apps grandes.