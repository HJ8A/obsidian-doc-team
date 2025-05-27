
##  **Paso 1: Conectar Frontend y Backend**

### **1. En Angular (frontend)**, crea un servicio para llamadas HTTP:
```bash
ng generate service services/api
```

Ejemplo de `api.service.ts`:
```typescript
import { HttpClient } from '@angular/common/http';

@Injectable()
export class ApiService {
  constructor(private http: HttpClient) {}

  getBooks() {
    return this.http.get('http://localhost:3000/books');
  }
}
```

### **2. En NestJS (backend)**, crea un controlador básico:
```typescript
// books.controller.ts
@Controller('books')
export class BooksController {
  @Get()
  getBooks() {
    return [{ title: 'El Principito', author: 'Antoine de Saint-Exupéry' }];
  }
}
```

## 1. **Crear un usuario y base de datos para tu proyecto**:

```bash
sudo -u postgres psql -c "CREATE USER mi_usuario WITH PASSWORD 'mi_contraseña' CREATEDB;"
sudo -u postgres psql -c "CREATE DATABASE masterpage_db OWNER mi_usuario;"
```
>Reemplazar *mi_usuario* , *mi_contraseña* y *masterpage_db* por sus datos

 Verificar conexión:
```bash
psql -h localhost -U mi_usuario -d masterpage_db
```
>Reemplazar *mi_usuario* y *masterpage_db* por sus datos
