README - Mobile Academic Management

1. Descripción general del proyecto
------------------------------------
Mobile Academic Management (MAM) es una aplicación móvil desarrollada en Android Studio con Kotlin, cuyo propósito es optimizar y facilitar la gestión académica a través de una plataforma intuitiva. Está diseñada para tres tipos de usuarios: estudiantes, profesores y personal administrativo. Entre sus principales funcionalidades se encuentran la creación de clases, el control de asistencia mediante códigos QR, la consulta de horarios, y el manejo de información académica de manera centralizada.

Este proyecto forma parte de una iniciativa educativa enfocada en digitalizar procesos escolares para mejorar la eficiencia, la comunicación y la experiencia de los usuarios dentro del entorno académico.

2. Requisitos del sistema
---------------------------
Para compilar y ejecutar correctamente esta aplicación, se necesita:
- Android Studio instalado.
- SDK de Android versión 33 o superior.
- Gradle 7.4 o más reciente.
- Kotlin versión 1.8 o superior.
- Dispositivo físico o emulador con Android 10 (API 29) o superior.
- Acceso a internet para permitir la conexión con Firebase.
- Archivo `google-services.json` configurado correctamente para la autenticación y base de datos.

3. Instrucciones de instalación
--------------------------------------------------------
Sigue los pasos a continuación para configurar y ejecutar la aplicación:

1. Descarga o clona el repositorio desde su fuente.
2. Abre el proyecto en Android Studio.
3. Espera a que el IDE sincronice los archivos Gradle automáticamente.
4. Verifica que los paquetes de Kotlin y Firebase estén correctamente instalados.
5. Ejecuta la aplicación en un dispositivo o emulador desde el botón “Run”.

Nota: El proyecto está diseñado para trabajar con Firebase, por lo que es importante tener configurado un proyecto en la consola de Firebase con autenticación y base de datos habilitadas.

4. Ejemplo de uso
------------------
- Para profesores: Pueden iniciar sesión y acceder a un panel donde pueden agregar nuevas clases, indicando días, horarios y salones. También pueden generar y mostrar códigos QR para registrar la asistencia de los alumnos.
- Para estudiantes: Tienen acceso a escanear los códigos QR proporcionados por el profesor para registrar su asistencia. También pueden consultar el listado de clases asignadas.
- Para personal administrativo: Pueden revisar la información almacenada sobre usuarios y actividades, aunque esta funcionalidad puede ser ampliada dependiendo del tipo de permisos definidos en Firebase.

5. Descripción general de los componentes
------------------------------------------
- `MainActivity`: actividad de entrada que direcciona según el tipo de usuario.
- `LoginActivity`: permite a los usuarios autenticarse usando Firebase Authentication.
- `RegisterActivity`: permite el registro de nuevos usuarios con roles definidos.
- `SaveInfoClass`: interfaz que permite a los profesores crear clases especificando nombre, horario, días y aula.
- `ResultInformation`: muestra en un RecyclerView todas las clases agregadas por el usuario activo.
- `AttendanceActivity`: vista que muestra los registros de asistencia de los estudiantes, con nombre, hora y estado (asistencia confirmada).
- `AttendanceAdapter`: adapta la información para visualizarla de forma estructurada en tarjetas (CardView).
- `Firebase Realtime Database`: almacena información en tiempo real como usuarios, clases y asistencia.
- `google-services.json`: archivo clave para conectar la app con Firebase.

Este proyecto sirve como una base sólida para ampliar funcionalidades académicas digitales y puede integrarse con otras soluciones institucionales en el futuro.
