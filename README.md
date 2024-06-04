# 🖥️ Mi proyecto SmartThinker 📱
Este readme incluye lo siguiente

## Tabla de contenido 🚀
- [Introduccion al proyecto](#introduccion-al-proyecto)
- [Instrucciones de instalación y ejecución.](#instrucciones-de-instalación-y-ejecución)
- [Descripción del proyecto (estructura y uso del proyecto Web)](#descripción-del-proyecto-estructura-y-uso-del-proyecto-web)
- [Descripción del proyecto (estructura y uso del proyecto Movil)](#descripción-del-proyecto-estructura-y-uso-del-proyecto-movil)
- [Prototipos de la vista y cómo utilizarlas (tipo manual)](#prototipos-de-la-vista-y-cómo-utilizarlas-tipo-manual)
- [Descripción de las pruebas y cómo ejecutarlas.](#prototipos-de-la-vista-y-cómo-utilizarlas-tipo-manual)
- [URL de despliegue en Vercel.](#url-de-despliegue-en-vercel)

# Introduccion al proyecto

Mi proyecto el cual principalmente es movil consta de dos partes, la parte de mi Backend que se encuentra en el repositorio [SmartThinker-Backendo](https://github.com/KatoGC/SmartThinkerBackendo.git?authuser=1) el cual esta desarrollo en [Strapi](https://strapi.io/) y la parte del Frontend que se encuentra el repositorio [SmartThinkerWeb](https://github.com/KatoGC/SmartThinkerWeb.git?authuser=1) asi como la parte Movil en el repositorio [SmartThinkerApp](https://github.com/KatoGC/SmartThinkerApp). 🤖

# Instrucciones de instalación y ejecución.

## 🛠️ Requisitos de instalacion 🛠️ 

Asegurarse de tener instalado Node.js

- [Node.js](https://nodejs.org/en)

Para la parte movil tener instalado Android Studio

- [Android Studio](https://developer.android.com/studio)

### Clonar el repositorio
De la aplicacion Web:

```sh
   git clone https://github.com/KatoGC/SmartThinkerWeb.git?authuser=1
```
De la aplicacion Molvi 
```sh
   git clone https://github.com/KatoGC/SmartThinkerApp
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

Frontend Web con [Vite](https://vitejs.dev/guide) 
```sh
    npm run dev
```

Frontend Movil con [React Native](https://reactnative.dev/) E inciializar nuestro Android Studio con su respectivo emulador
``` sh
   npm start
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
# 📱Descripción del proyecto (estructura y uso del proyecto Movil)📱
El proyecto consta de un registro de usuarios, login, la pantalla de Home, pantalla de cursos y actividades, pantalla de notificaciones, pantalla de usuario y pantalla para editar los datos del usuario.
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
Se muestran los datos del usuario ademas que se agrega el boton para para editar el perfil el cual nos redirige a la pantalla de editar y un boton para cerrar sesion, asi como regresar a la screen de Home.
```
### CoursesScreen
```
Se visualizan los cursos, aun no tiene la funcion de crear curso ni de redigirir a screen de CreateCourses.
```
### Actividades
``` 
Se visualizan las actividades, aun no tiene la funcion de crear actividad ni de redigirir a screen de CreateActivity.
```
### HomeScreen
```
Es la screen Home donde se ven los cursos y actividades disponibles.
```

### EditProfile 
```
Se muestran los datos del usuario ademas que se agrega la funcion para editarlos o cancelar.
```
### Notificaciones
```
Se visualizan las notificaciones, de momento no existe tal atributo en el backend asi que solamente es algo visual por parte del front.
```
# URL de despliegue en Vercel.
De momento no pude realizar el despliegue.
