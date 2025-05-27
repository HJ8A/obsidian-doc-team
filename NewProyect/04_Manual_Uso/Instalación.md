
Pasos para construir el proyecto desde 0 - LINUX

##  **Paso 1: Instale Node.js y npm desde los repositorios oficiales:**

 ```bash
sudo pacman -S nodejs npm
 ```

Instalación del Frontend (Angular, Material, Chart.js)
 ```bash
 npm install -g @angular/cli
 ```
 
Verificar la instalación
 ```bash
ng version
node -v
npm -v
 ```

## **Paso 2: Instalar el Backend (NestJS )

Instalar NestJs CLI
 ```bash
 npm install -g @angular/cli
 ```

Verificar la instalación
 ```bash
nest --version
 ```

---
## **Paso 3: Crear el proyecto [[Angular]]

Ubicarse en la carpeta donde se creará el proyecto ()
 ```bash
ng new frontend
 ```

Instalar Angular (en la terminal consola  )
 ```bash
ng add @angular/material
 ```

configuración básica de Material
 ```typescript
import { MatButtonModule } from '@angular/material/button';
import { MatCardModule } from '@angular/material/card';

@NgModule({
  imports: [MatButtonModule, MatCardModule],
})
export class AppModule { }
 ```

Ejecutar el servidor de desarrollo
```bash
ng serve
 ```
>Abre tu navegador en `http://localhost:4200`)
## **Paso 4: Crear el proyecto [[NestJS]]

```bash
nest new backend
 ```

Instalar [[Prisma]] (ORM)
```bash
npm install prisma @prisma/client
npx prisma init
 ```
>Esto crea un archivo `prisma/schema.prisma` y configura `.env`.

Configurar Prisma con [[PostgreSQL]] (Edita `prisma/schema.prisma`:)
```env
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL") // Definida en .env
}
 ```

Ejemplo de `.env`:

Ejecutar el servidor [[NestJS]]
```bash
npm run start:dev
 ```
>El backend estará en `http://localhost:3000`.

## **Paso 4: Instalar [[PostgreSQL]]

**Instala el paquete** para arch linux (incluye servidor y cliente CLI): 
```bash
sudo pacman -S postgresql
 ```

**Inicializa el cluster de la base de datos**:
```bash
sudo su - postgres -c "initdb --locale en_US.UTF-8 -D /var/lib/postgres/data"
 ```

**Habilita e inicia el servicio**:
```bash
sudo systemctl enable --now postgresql.service
 ```

**Verifica que esté corriendo**:
```bash
sudo systemctl status postgresql.service
 ```