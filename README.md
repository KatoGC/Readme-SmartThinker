# 🖥️ Mi proyecto SmartThinker 📱
Este readme incluye lo siguiente

## Tabla de contenido 🚀
- [Introduccion al proyecto](#introduccion-al-proyecto)
- [Instrucciones de instalación y ejecución.](#instrucciones-de-instalación-y-ejecución)
- [Descripción del proyecto (estructura y uso del proyecto Web)](#descripción-del-proyecto-estructura-y-uso-del-proyecto-web)
- [Prototipos de la vista y cómo utilizarlas (tipo manual)](#prototipos-de-la-vista-y-cómo-utilizarlas-tipo-manual)
- [Descripción de las pruebas y cómo ejecutarlas.](#prototipos-de-la-vista-y-cómo-utilizarlas-tipo-manual)
- [URL de despliegue en Vercel.](#url-de-despliegue-en-vercel)

# Introduccion al proyecto

Mi proyecto el cual principalmente es movil consta de dos partes, la parte de mi Backend que se encuentra en el repositorio [SmartThinker-Backendo](https://github.com/KatoGC/SmartThinkerBackendo.git?authuser=1) el cual esta desarrollo en [Strapi](https://strapi.io/) y la parte del Frontend que se encuentra el repositorio [SmartThinkerWeb](https://github.com/KatoGC/SmartThinkerWeb.git?authuser=1). 🤖

# Instrucciones de instalación y ejecución.

## 🛠️ Requisitos de instalacion 🛠️ 

Asegurarse de tener instalado Node.js

- [Node.js](https://nodejs.org/en)

### Clonar el repositorio
De la aplicacion Web:

```sh
   git clone https://github.com/KatoGC/SmartThinkerWeb.git?authuser=1
```
 y Backend en la máquina local:
```sh
   git clone https://github.com/KatoGC/SmartThinkerBackendo.git?authuser=1
 ```
### 💻 Instalacion de cada proyecto una vez clonado 💻
Para Vite, ReactNative y Strapi utiliza el mismo comando
```sh
   npm install
```
### Ejecucion de cada proyecto
Backend con [Strapi](https://strapi.io/) comando que permite la modificacion de entidades y atributos mientras esta en funcionamiento
```sh
    npm run develop
```

Frontend con [Vite](https://vitejs.dev/guide) 
```sh
    npm run dev
```
# 📕Descripción del proyecto (estructura y uso del proyecto WEB)📕
El proyecto consta de un registro de usuarios, login, la pantalla de usuario, vista de cursos y creacion de estos.
# Prototipos de la vista y cómo utilizarlas (tipo manual)
Consta de 
### Login
``` 
Es basicamente donde se llena el campo de  email y password para ingresar a la aplicacion.
```
### SignUp
```
Donde se registra el usuario
```

### UserProfile 
```
Se muestran los datos del usuario ademas que se agrega el boton para navegar al componente de cursos y otro para cerrar sesion.
```
### Cursos
```
Se visualizan los cursos creados, descripcion de ellos y un boton para crear cursos nuevos o regresar al perfil.
```
# Descripción de las pruebas y cómo ejecutarlas.
Se crearon dos test en el componente UserProfile

## 🧪 Tests Específicos 🧪

### fetches and displays user data correctly

```
1. Simulación: Se configura la API simulada para que devuelva datos de usuario predefinidos (userData).

2. Renderizado: Se renderiza el componente UserProfile.

3. Esperas (waitFor y waitForElementToBeRemoved): Se utiliza waitForElementToBeRemoved para esperar a que desaparezca el mensaje "Cargando...". Luego, waitFor espera a que los datos del usuario se muestren en la pantalla.

4. Verificaciones: Se comprueba que todos los campos (nombre, email, edad, ocupación, descripción) se muestren correctamente con los datos proporcionados por la API simulada.
```
### logs out user on button click
```
1. Simulación: Se configura la API para que responda con datos vacíos (no son relevantes para este test).

2. Renderizado: Se renderiza el componente UserProfile. Esperas (waitFor): Espera a que el botón "Cerrar Sesión" esté presente en la pantalla.

3. Interacción (userEvent): Se simula un clic en el botón "Cerrar Sesión".

4. Verificaciones:Se verifica que localStorage.removeItem se haya llamado con la clave "jwt" para simular la eliminación del token. Se verifica que mockNavigate se haya llamado con la ruta "/login", lo que indica que se intentó redirigir al usuario a la pantalla de inicio de sesión.
```
# URL de despliegue en Vercel.
De momento no pude realizar el despliegue.