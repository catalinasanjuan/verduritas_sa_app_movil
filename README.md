# Verduritas SA

Verduritas SA es una aplicación móvil desarrollada en Android Studio para la gestión y registro de cultivos. La app permite a los usuarios registrar y visualizar cultivos, así como autenticarse utilizando Firebase Authentication. La aplicación utiliza un diseño atractivo y una paleta de colores acorde a la temática natural.

## Características Principales

1. **Autenticación de Usuarios:**
    - Registro e inicio de sesión mediante Firebase Authentication.
    - Integración con Google Sign-In.

2. **Gestión de Cultivos:**
    - Registro de nuevos cultivos con datos como tipo de cultivo, fecha de cultivo y fecha estimada de cosecha.
    - Visualización de la lista de cultivos registrados.

3. **Interfaz de Usuario:**
    - Diseño con una paleta de colores pastel, basada en tonos verdes, para reflejar la temática de la naturaleza.
    - Botones personalizados y una experiencia de usuario sencilla y clara.

## Requisitos del Sistema

- **Sistema Operativo:** Android 6.0 (API 23) o superior.
- **IDE:** Android Studio Electric Eel o superior.
- **Dependencias:**
    - Firebase Authentication
    - Firebase Firestore (opcional para almacenamiento de datos)

## Instalación

1. Clona este repositorio:

   ```bash
   git clone https://github.com/tu_usuario/verduritas_sa.git
   ```

2. Abre el proyecto en Android Studio.

3. Asegúrate de que el archivo `google-services.json` esté ubicado en la carpeta `app` para la integración con Firebase.

4. Sincroniza el proyecto con Gradle:
    - Ve a `File > Sync Project with Gradle Files`.

5. Conecta un dispositivo físico o inicia un emulador de Android.

6. Ejecuta la aplicación:
    - Ve a `Run > Run 'app'` o presiona **Shift + F10**.

## Configuración de Firebase

1. Accede a la consola de Firebase: [https://console.firebase.google.com](https://console.firebase.google.com)
2. Crea un nuevo proyecto llamado "Verduritas SA".
3. Agrega una aplicación de Android e introduce el nombre del paquete:
    - `catalina.sanjuan.verduritassa`
4. Descarga el archivo `google-services.json` y colócalo en la carpeta `app` del proyecto.
5. Habilita Firebase Authentication y configura los proveedores necesarios (correo y Google).

## Arquitectura

La aplicación sigue una estructura básica de capas:

- **UI:** Maneja las vistas (archivos XML) y las interacciones del usuario.
- **Lógica:** Actividades como `MaiinActivity`, `CultivoActivity` y `LiistaCultivosActivity` contienen la lógica de negocio.
- **Modelos:** La clase `Cultivo` se utiliza para manejar los datos relacionados con los cultivos.

## Estructura de Carpetas

```
app/
├── java/
│   └── catalina/
│       └── sanjuan/
│           └── verduritassa/
│               ├── Cultivo.java
│               ├── CultivoActivity.java
│               ├── CultivoAdapter.java
│               ├── LiistaCultivosActivity.java
│               └── MaiinActivity.java
├── res/
│   ├── drawable/
│   ├── layout/
│   │   ├── activity_cultivo.xml
│   │   ├── activity_lista_cultivos.xml
│   │   ├── activity_login.xml
│   │   ├── activity_register.xml
│   │   └── item_cultivo.xml
│   ├── values/
│   │   ├── colors.xml
│   │   ├── strings.xml
│   │   ├── styles.xml
│   │   └── themes.xml
└── google-services.json
```

## Dependencias Clave

```gradle
// Firebase
implementation platform('com.google.firebase:firebase-bom:33.5.1')
implementation 'com.google.firebase:firebase-auth-ktx'
implementation 'com.google.firebase:firebase-analytics'

// Material Components
implementation 'com.google.android.material:material:1.5.0'

// ConstraintLayout
implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
```

## Paleta de Colores

| Nombre          | Código Hex |
|-----------------|------------|
| Fondo principal | `#EAF4E3`  |
| Botones         | `#A3CFA7`  |
| Texto principal | `#424242`  |
| Detalles        | `#6D6875`  |

## Usuario

**Login**
- **User:**  clases.inacap.mafer@gmail.com
- **Password:** inacap2024

## Contribución

Si deseas contribuir al proyecto, por favor abre un issue o crea un pull request.

## Licencia

Este proyecto está bajo la Licencia MIT. Para más información, consulta el archivo LICENSE.

