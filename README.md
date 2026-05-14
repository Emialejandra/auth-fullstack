
# Sistema Auth Fullstack

## Descripción

Este proyecto consiste en un sistema de autenticación Fullstack desarrollado con:

- Frontend en React + Vite
- Backend en Node.js + Express
- Base de datos MongoDB Atlas
- Encriptación de contraseñas con bcryptjs
- Tokens JWT para verificación y recuperación de contraseña

El sistema permite:

- Registro de usuarios
- Verificación de cuenta mediante token
- Solicitud de recuperación de contraseña
- Generación de token para restablecer contraseña
- Restablecimiento de contraseña usando JWT

---

# Tecnologías Utilizadas

## Frontend
- React
- Vite
- CSS
- React Router DOM

## Backend
- Node.js
- Express
- Mongoose
- bcryptjs
- jsonwebtoken
- cors
- nodemon

## Base de Datos y Autenticación
- MongoDB Atlas

---

# Estructura del Proyecto

```txt
auth-fullstack/
│
├── backend/
│   ├── controllers/
│   │   └── auth.controller.js
│   │
│   ├── models/
│   │   └── User.js
│   │
│   ├── routes/
│   │   └── auth.routes.js
│   │
│   ├── .env
│   ├── server.js
│   └── package.json
│
├──frontend/
│  ├── public/
│  ├── src/
│  |   └── assets/
│  |   │
│  |   ├── pages/
│  |   │   ├── ForgotPassword.jsx
│  |   │   ├── Register.jsx
│  |   │   ├── ResetPassword.jsx
│  |   │   └── VerifyAccount.jsx
│  |   │
│  |   ├── services/
│  |   │   └── authService.js
│  |   │
│  |   ├── App.css
│  |   ├── App.jsx
│  |   ├── index.css
│  |   └── main.jsx
│  |
|  ├── package.json
│  |
|  ├── README.md

```

---

# Instalación del Proyecto

## 1. Clonar repositorio

```bash
git clone https://github.com//ProyectoWeb.git 
```

---

# Configuración Backend

Entrar a la carpeta backend:

```bash
cd backend
```

Instalar dependencias:

```bash
npm install
```

Iniciar servidor:

```bash
npm run dev
```
## Backend ejecutándose en: 
```bash
http://localhost:3000
```
---

# Configuración Frontend

Entrar a la carpeta frontend:

```bash
cd frontend
```

Instalar dependencias:

```bash
npm install
```

Ejecutar proyecto:

```bash
npm run dev
```
## Frontend ejecutándose en:
```bash
http://localhost:5173
```
---


# Funcionalidades

El sistema permite registrar nuevos usuarios mediante:
- Nombre
- Correo electrónico
- Contraseña

Durante el registro:
- se validan los campos
- Se verifica que el correo no exista
- La contraseña se encripta con bcryptjs
- Se genera un token JWT de verificación
- Los datos son almacenados en MongoDB Atlas

---
# API Endpoints

## Registrar usuario

POST `/api/auth/register`

Body:

```json
{
  "name": "Emilia",
  "email": "emilia@test.com",
  "password": "123456"
}
```

---

## Verificar cuenta

GET `/api/auth/verify/:token`

---

## Recuperar contraseña

POST `/api/auth/forgot-password`

Body:

```json
{
  "email": "emilia@test.com"
}
```

---

## Restablecer contraseña

POST `/api/auth/reset-password/:token`

Body:

```json
{
  "newPassword": "12345678"
}
```

---

# Evidencia

- Módulo Registro
  
<img width="883" height="512" alt="Captura de pantalla 2026-05-13 151358" src="https://github.com/user-attachments/assets/d8bb5540-baf7-41a0-95e9-3ad1ce15d725" />
   
- Módulo Recuperar contraseña

<img width="865" height="479" alt="Captura de pantalla 2026-05-13 152747" src="https://github.com/user-attachments/assets/ba56aea1-eea5-41f9-98d3-ae38b2b70f0e" />
  
---
# Autor

Emilia Tana 

---

# Materia

Desarrollo de Aplicaciones Web

---

# Estado del Proyecto

En desarrollo

---
