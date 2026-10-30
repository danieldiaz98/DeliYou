# DeliYou

![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?logo=kotlin&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Auth%20%2B%20Firestore-FFCA28?logo=firebase&logoColor=black)
![SQLite](https://img.shields.io/badge/SQLite-Local-003B57?logo=sqlite&logoColor=white)
![Android](https://img.shields.io/badge/Android-SDK%2032-3DDC84?logo=android&logoColor=white)

Aplicación Android de pedidos de comida desarrollada en **Kotlin**. Permite explorar restaurantes, consultar sus menús, gestionar un carrito y guardar favoritos, con autenticación y datos en la nube mediante **Firebase**.

<p align="center">
  <img src="https://user-images.githubusercontent.com/91387558/207674658-6bac22fe-2974-446f-93a4-36bef3ae6cef.png" alt="Captura de DeliYou">
</p>

## Características

- **Registro y login** con email y contraseña (Firebase Auth).
- **Inicio de sesión con Google** (Google Sign-In).
- **Listado de restaurantes** desde Firestore con RecyclerView y adaptadores personalizados.
- **Detalle de restaurante** con menú y productos.
- **Carrito de la compra** persistido en SQLite local.
- **Favoritos** de restaurantes guardados en SQLite.
- **Historial de pedidos**.
- **Alta de restaurantes** mediante formulario conectado a Firebase.
- **Navegación** con DrawerLayout y NavigationView.
- **Carga de imágenes** remota con Picasso.
- Interfaz Material Design con temas claro/oscuro.

## Stack

| Componente | Tecnología |
| --- | --- |
| Lenguaje | Kotlin |
| Plataforma | Android (minSdk 21, targetSdk 32) |
| Autenticación | Firebase Auth + Google Sign-In |
| Base de datos remota | Firebase Firestore / Realtime Database |
| Base de datos local | SQLite (`SQLiteOpenHelper`) |
| Imágenes | Picasso |
| UI | Material Components, RecyclerView, DrawerLayout |

## Estructura del proyecto

```text
DeliYou/
├── app/
│   └── src/
│       ├── main/
│       │   ├── java/pmn/dev/deliyou/
│       │   │   ├── MainActivity.kt        # Pantalla de bienvenida / login
│       │   │   ├── LoginActivity.kt
│       │   │   ├── RegisterActivity.kt
│       │   │   ├── MainPage.kt            # Listado de restaurantes
│       │   │   ├── RestaurantDetail.kt    # Menú del restaurante
│       │   │   ├── Favoritos2.kt
│       │   │   ├── pedidos.kt
│       │   │   ├── form_restaurantdb.kt
│       │   │   ├── CartDB.kt              # Persistencia del carrito
│       │   │   ├── FavDB.kt               # Persistencia de favoritos
│       │   │   ├── *Adapter.kt            # Adaptadores de RecyclerView
│       │   │   └── *Item.kt / *.kt        # Modelos de datos
│       │   ├── res/                       # Layouts, drawables, temas, strings
│       │   └── AndroidManifest.xml
│       ├── test/                          # Tests unitarios
│       └── androidTest/                   # Tests instrumentados
├── build.gradle
├── settings.gradle
└── gradle/
```

## Requisitos

- Android Studio (versión reciente)
- JDK 8 o superior
- Un proyecto de Firebase con Authentication, Firestore y Realtime Database habilitados

## Configuración

1. Clona el repositorio y ábrelo en Android Studio:

   ```bash
   git clone https://github.com/danieldiaz98/DeliYou.git
   ```

2. Crea un proyecto en [Firebase Console](https://console.firebase.google.com/) con el paquete `pmn.dev.deliyou`.

3. Descarga el archivo `google-services.json` y colócalo en `app/`.

   > Este archivo contiene la configuración del proyecto Firebase y está ignorado por Git. Cada desarrollador debe usar el suyo.

4. Habilita en Firebase:
   - **Authentication** (Email/Password y Google)
   - **Firestore Database**
   - **Realtime Database**

5. Sincroniza Gradle y ejecuta la app en un emulador o dispositivo.

## Build

```bash
./gradlew assembleDebug
```

El APK se genera en `app/build/outputs/apk/debug/`.

## Diseño y planificación

- **Figma:** [Prototipo de la interfaz](https://www.figma.com/file/gOHwaOla4qvu6YPrWyWm41/Untitled)
- **Trello:** [Tablero del proyecto](https://trello.com/b/LBDU8vw0/deliyou)
- **Roadmap:** [Documentación del equipo](https://github.com/NestorManeiro/AndroidStudio/blob/main/README.md)

## Contexto

Proyecto desarrollado para la asignatura de **Programación de Medios y Navegadores (PMN)** por un equipo de estudiantes, usando Kotlin y Firebase.

## Licencia

Proyecto con fines educativos y de portfolio. Consulta con los autores antes de un uso comercial.
