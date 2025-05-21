# 🔐 ¿Qué es Passport.js?

**Passport.js** es un **middleware de autenticación** para Node.js. Es **modular, flexible y extremadamente popular**, ya que soporta muchos tipos de autenticación con **estrategias** reutilizables.

> 📌 Permite autenticar usuarios mediante:
> 
> - Usuario/contraseña
>     
> - OAuth (Google, Facebook, Twitter, GitHub)
>     
> - JWT (JSON Web Tokens)
>     
> - Tokens API, SSO, etc.
>     

---

## 🎯 ¿Para qué sirve Passport?

- Iniciar sesión con usuario y contraseña.
    
- Autenticarse con redes sociales.
    
- Usar tokens JWT para proteger rutas.
    
- Implementar sesiones (logins persistentes).
    

---

## 🧱 ¿Cómo funciona Passport?

1. **Instalas Passport** y una **estrategia** (ej: local, JWT, Google, etc).
    
2. Configuras el middleware de autenticación en tu app.
    
3. Definís cómo verificar un usuario (ej: buscarlo en base de datos).
    
4. Usás Passport para proteger rutas privadas.
    

---

## 🛠️ Estrategias más comunes

|Estrategia|¿Para qué sirve?|
|---|---|
|`passport-local`|Usuario + contraseña (login clásico)|
|`passport-jwt`|JWT tokens (para APIs modernas)|
|`passport-google-oauth20`|Login con Google|
|`passport-facebook`|Login con Facebook|
|`passport-github2`|Login con GitHub|

---

## 🔧 Ejemplo básico con `passport-local` (Express)

### 1. Instalación:

`npm install passport passport-local express-session`

### 2. Configurar Passport

const passport = require('passport');
const LocalStrategy = require('passport-local').Strategy;

passport.use(new LocalStrategy((username, password, done) => {
  // Aquí iría la lógica de autenticación
  const user = { id: 1, username: "admin", password: "1234" };
  if (username === user.username && password === user.password) {
    return done(null, user);
  }
  return done(null, false, { message: 'Credenciales incorrectas' });
}));

// Serialización (guarda el usuario en sesión)
passport.serializeUser((user, done) => {
  done(null, user.id);
});
passport.deserializeUser((id, done) => {
  // Buscar el usuario por ID en la base de datos
  done(null, { id: 1, username: "admin" });
});


### 3. Middleware en Express

const express = require('express');
const session = require('express-session');
const app = express();

app.use(express.urlencoded({ extended: false }));
app.use(session({ secret: 'mi-clave-secreta', resave: false, saveUninitialized: false }));
app.use(passport.initialize());
app.use(passport.session());

### 4. Ruta de login

app.post('/login', passport.authenticate('local', {
  successRedirect: '/perfil',
  failureRedirect: '/login'
}));

---

## 🔐 Protección de rutas

function estaAutenticado(req, res, next) {
  if (req.isAuthenticated()) return next();
  res.redirect('/login');
}

app.get('/perfil', estaAutenticado, (req, res) => {
  res.send(`Bienvenido, ${req.user.username}`);
});


---

## ✅ Passport en NestJS

NestJS tiene un módulo oficial llamado `@nestjs/passport` y funciona muy bien con JWT. Si te interesa, te puedo preparar una plantilla completa de **NestJS + Passport + JWT + Roles**.

---

## 🧠 Ventajas de Passport.js

|Ventaja|Descripción|
|---|---|
|Modular|Puedes cambiar o combinar estrategias fácilmente|
|Ampliamente usado|Bien documentado, con soporte para docenas de estrategias|
|Compatible con Express|Se integra fácilmente|
|Soporta sesiones y JWT|Ambas formas de autenticación modernas|

---

## ⚠️ Consideraciones

- Si usás JWT, **no necesitas sesiones** (es stateless).
    
- Si usás redes sociales, tendrás que registrar tu app en cada proveedor.
    
- Passport no encripta contraseñas: **usa bcrypt o argon2** por separado.