# prueba#  Event Manager SPA

Este proyecto es una Single Page Application (SPA) desarrollada con JavaScript Vanilla. Permite a los usuarios registrarse en eventos, y a los administradores crear y editar eventos.

---

##  Requisitos

- [Node.js](https://nodejs.org/)
- [json-server](https://www.npmjs.com/package/json-server)
- Navegador moderno
- (Opcional) Live Server de VSCode

---

##  Instalación y ejecución

1. **Clona el repositorio o descarga los archivos.**

2. **Instala `json-server` si no lo tienes:**

```bash
npm install -g json-server
```

3. **Ubica el archivo `db.json` y ejecuta el servidor JSON:**

```bash
json-server --watch db.json --port 3000
```

Esto iniciará una API REST simulada en:

```
http://localhost:3000/events
```

4. **Abre `index.html` en tu navegador:**

Recomendado usar **Live Server** en VSCode.  
Evita abrirlo directamente como archivo (`file://`) si usas módulos ES6 (`type="module"` en el script).

---

## Navegación de rutas

| Ruta                                | Descripción                         |
|-------------------------------------|-------------------------------------|
| `#/login`                           | Vista de inicio de sesión           |
| `#/register`                        | Vista de registro                   |
| `#/`                                | Vista principal con eventos         |
| `#/dashboard/events/enrollments`   | Registro a eventos (solo visitantes)|
| `#/editorView`                      | Formulario para editar evento       |

---

## Roles

| Rol     | Acciones disponibles                          |
|---------|-----------------------------------------------|
| `admin` | Crear y editar eventos. No accede a inscripciones |
| `visitor` | Registrarse a eventos. No puede editar        |

---

## Estructura del proyecto

```
JavaScript-test-main/
│
├── app/
│   ├── assets/css/styles.css
│   └── js/
│       ├── auth.js
│       ├── routes.js
│       ├── API/
│       │   ├── API.js
│       │   └── eventsAPI.js
│       └── views/
│           ├── dashboard.js
│           ├── enrollments.js
│           ├── editorEvents.js
│           ├── login.js
│           ├── register.js
│           └── notFound.js
│
├── db.json
├── index.html
├── index.js
└── README.md
```

---

## Tips

- Si ves un error relacionado a `createView` o módulos, asegúrate de que esté bien exportado/importado.
- El formulario de edición (`editorView`) rellena automáticamente los datos desde `localStorage`.
- Usa el `router.js` para manejar la navegación sin recargar la página.

---

##  Autor

Desarrollado por **Mariana Restrepo**
Clan: ####
CC: ####
Email: ####  
Proyecto para práctica de SPA con autenticación y gestión de eventos.
