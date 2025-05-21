## **3. Estructura de Tablas (Modelo Lógico)**

 **Tabla: `usuarios`**

- id (PK)
- nombre
- email
- contraseña
- rol_id (FK → roles.id)

**Tabla: `roles`**
- id (PK)
- nombre

**Tabla: `clientes`**
- id (PK)
- nombre
- dni
- email (opcional)
- telefono (opcional)
**Tabla: `categorias`**
- id (PK)
- nombre

**Tabla: `productos`**

- id (PK)
- nombre
- descripcion
- precio_unitario
- stock
- categoria_id (FK → categorias.id)
    

**Tabla: `ventas`**
- id (PK)
- fecha
- total
- usuario_id (FK → usuarios.id)
- cliente_id (FK → clientes.id)

**Tabla: `detalles_venta`**

- id (PK)
- venta_id (FK → ventas.id)
- producto_id (FK → productos.id)
- cantidad
- precio_unitario
- subtotal
    

**Tabla: `proveedores`** (opcional)

- id (PK)
- nombre
- ruc  
- direccion
- telefono

**Tabla: `inventario`**

- id (PK)
- producto_id (FK → productos.id)
- cantidad
- fecha_actualizacion