# Tienda 3479

Página web conectada a la base Oracle `DB_TIENDA3479` (Oracle 23ai Free, servicio `FREEPDB1`).

## Cómo ejecutar

```
npm install
npm start
```

Abrir http://localhost:3000

## Estructura

```
.env               Credenciales de la base de datos
src/db.js          Pool de conexiones a Oracle
src/server.js      Servidor Express + API REST
public/            Página web (HTML, CSS, JS)
requests.http      Ejemplos de llamadas a la API
```

## API

| Método | Ruta                  | Acción              |
|--------|-----------------------|---------------------|
| GET    | /api/estado           | Estado de conexión  |
| GET    | /api/productos        | Listar productos    |
| GET    | /api/productos/:id    | Obtener un producto |
| POST   | /api/productos        | Crear producto      |
| PUT    | /api/productos/:id    | Actualizar producto |
| DELETE | /api/productos/:id    | Eliminar producto   |

Las mismas rutas existen para `/api/clientes`.

Cuerpo JSON de producto: `{ "NOMBRE": "...", "PRECIO": 10.5, "STOCK": 3 }`
Cuerpo JSON de cliente: `{ "NOMBRE": "...", "NIT_DPI": "...", "CORREO": "..." }`
