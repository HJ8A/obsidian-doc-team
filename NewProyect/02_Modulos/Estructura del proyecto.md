
sistema-gestion-libreria/
├── frontend/               # Angular (UI)
│   ├── src/
│   │   ├── app/
│   │   │   ├── services/   # Llamadas al backend
│   │   │   └── components/ # Componentes Material
├── backend/                # NestJS (API)
│   ├── src/
│   │   ├── auth/           # Autenticación JWT
│   │   ├── prisma/         # Modelos de DB
│   │   └── main.ts         # Punto de entrada