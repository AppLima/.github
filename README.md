# InLima - Grupo 4 🚀
## Entorno de desarrollo 💻

### Breve descripción del entorno de desarrollo

El entorno de desarrollo utilizado para la aplicación **InLima** se basa en Flutter, una tecnología de desarrollo multiplataforma que permite crear aplicaciones móviles eficientes para iOS y Android. Además, se utiliza **Android Studio** para la gestión de emuladores y SDKs necesarios para el desarrollo en dispositivos Android.

### Descarga e instalación del SDK de Flutter
Para instalar Flutter, se debe comenzar descargando el SDK desde la página oficial de Flutter, [flutter.dev](https://flutter.dev). Se debe buscar el archivo ZIP correspondiente al sistema operativo y descargarlo. Luego, es necesario descomprimir el archivo en una ubicación adecuada, asegurándose de que la ruta donde se coloque no contenga espacios ni caracteres especiales.

### Configuración de variables de entorno
Después de descomprimir el SDK, se deben configurar las variables de entorno para que el sistema reconozca los comandos de Flutter. Para ello, se deben abrir las propiedades del sistema accediendo a través del **Panel de control**, entrando a **Sistema y seguridad**, luego a **Sistema**, y finalmente seleccionando **Configuración avanzada del sistema**.

En la ventana que aparece, se debe elegir la opción **Variables de entorno**. Dentro de la sección **Variables del sistema**, se busca la variable llamada **Path** y se hace clic en **Editar**. En la ventana de edición, se agrega una nueva entrada con la ruta completa a la carpeta `flutter/bin`, que se encuentra en el directorio donde se descomprimió el SDK. Una vez hecho esto, se deben guardar los cambios y cerrar todas las ventanas.

### Verificación de la instalación de Flutter
Luego, se abre una ventana de **Símbolo del sistema** o **PowerShell** y se ejecuta el comando `flutter doctor`. Este comando verificará si Flutter está instalado correctamente y si todos los componentes necesarios están presentes. El comando también proporcionará una lista de posibles problemas o pasos adicionales que se deben resolver, como la instalación de **Android SDK** o herramientas de desarrollo faltantes.

### Instalación de Android Studio
Dado que se desea desarrollar aplicaciones para Android, es necesario instalar **Android Studio**. Para ello, se debe visitar la [página oficial de Android Studio](https://developer.android.com/studio), descargar el instalador y seguir las instrucciones de instalación. Durante el proceso, es crucial asegurarse de seleccionar las opciones para instalar el **Android SDK** y el **Android Virtual Device (AVD)**.

Una vez que se haya completado la instalación de Android Studio, se debe abrir la aplicación y descargar cualquier paquete SDK adicional desde el **SDK Manager**.

### Pruebas de la aplicación en emulador o dispositivo físico
Para probar las aplicaciones desarrolladas en Flutter, se puede utilizar un emulador de Android o un dispositivo físico. En caso de preferir usar un dispositivo físico, se debe habilitar el **modo desarrollador** en el teléfono y activar la opción de **depuración USB**.

## Diagrama de despliegue 🌐
![Diagrama de despliegue](./assets/New%20folder/diagramadedespliegue.png)
## Requerimientos no funcionales 📋
#### RNF1 - Rendimiento:
- Las interfaces principales deben cargar en menos de 3 segundos con conexión 3G o superior.
- Soporte para 100 usuarios simultáneos sin pérdida de rendimiento.
- La latencia de comunicación con APIs externas (Google, Firebase, Cloud Storage) debe ser menor a 500 ms.

#### RNF2 - Seguridad:
- Cifrado de datos en reposo y en tránsito (HTTPS, AES 256 bits).
- Comunicación segura entre servicios (TLS/SSL) y almacenamiento cifrado de archivos adjuntos.
- Cumplimiento con normativas locales de protección de datos (ej. Ley N° 29733 en Perú).

#### RNF3 - Disponibilidad:
- Disponibilidad del sistema al 99.5% del tiempo anual.
- Tiempo de inactividad máximo de 24 horas por año.
- Plan de contingencia para fallos en servicios externos (APIs, Firebase, Cloud Storage).

#### RNF4 - Escalabilidad:
- Capacidad de escalar hasta 400 usuarios simultáneos.
- Permitir agregar nuevas funcionalidades o integrar servicios externos sin reescritura significativa.
- Manejo eficiente de mayores cargas de notificaciones y almacenamiento.

#### RNF5 - Usabilidad:
- Interfaz intuitiva y accesible (WCAG 2.1), con retroalimentación visual y auditiva.
- Formularios y botones claros para usuarios de todos los niveles.

#### RNF6 - Compatibilidad:
- Compatible con las últimas versiones de Android y distintos tamaños de pantalla.
- Adaptable a actualizaciones menores de APIs de Google (Maps, Facial Detection, Gmail).
- Interfaz responsiva para múltiples dispositivos.
## Diagrama de casos de uso 🛠️
![Diagrama de casos de uso](./assets/registrarseasd.png)
## Descripción de casos de uso 📝

### 1. Registro de Usuario
- **RF1:** El sistema debe permitir al ciudadano registrarse proporcionando correo, contraseña, DNI, nombre, apellidos y distrito actual.

![Diagrama de casos de uso](./assets/diagrama_casos_uso.png)
![Diagrama de casos de uso](./assets/registrarse%20Confirmaciónasd.png)

- **RF2:** El sistema debe permitir al ciudadano registrar o actualizar su rostro para utilizarlo como método de identificación.

![Diagrama de casos de uso](/assets/Identificador%20de%20rostro/agregadoasd.png)
![Diagrama de casos de uso](/assets/Identificador%20de%20rostro/agregando%202asd.png)
![Diagrama de casos de uso](/assets/Identificador%20de%20rostro/validación%20por%20emailasd.png)


### 2. Autenticación de Usuario
- **RF3:** El sistema debe permitir al usuario iniciar sesión validando el correo y la contraseña proporcionados con los datos de la base de datos.

![Diagrama de casos de uso](/assets/iniciar%20sesionasd.png)

- **RF4:** El sistema debe permitir al usuario iniciar sesión utilizando identificación facial.

![Diagrama de casos de uso](./assets/Iniciar%20sesion%20-%20Identificadorasd.png)
![Diagrama de casos de uso](/assets/Iniciar%20sesion%20-%20Identificador%20Registroasd.png)

- **RF5:** El sistema debe proporcionar una opción de recuperación de contraseña. Al hacer clic en "Olvidé mi contraseña", el usuario debe poder ingresar su correo electrónico para recibir un enlace de restablecimiento de contraseña.

![Diagrama de casos de uso](/assets/olvidaste%20tu%20contraseñaasd.png)
![Diagrama de casos de uso](/assets/olvidaste%20tu%20contraseña%20confirmacionasd.png)

### 3. Acceso al Menú Principal
- **RF6:** El sistema debe llevar al usuario al **menú principal** después de iniciar sesión, donde podrá acceder a las siguientes opciones:
   - **SOS:** Acceso rápido a servicios de emergencia (en caso sea ciudadano).
   - **Quejas/Sugerencias:** Permite generar y gestionar quejas.
   - **Sondeos:** Acceso a encuestas y votaciones.
   - **Historial:** Acceso al historial de quejas propio del usuario (en caso sea ciudadano).
 
![Diagrama de casos de uso](/assets/Homeasd.png)
![Diagrama de casos de uso](/assets/Home-adminasd.png)

### 4. Gestión de Quejas y Sugerencias
- **RF7:** El sistema debe permitir al ciudadano seleccionar el tipo de queja o sugerencia desde una lista de opciones predefinidas o la opción 'Otros'.

![Diagrama de casos de uso](/assets/Quejas%204_usuarioasd.png)

- **RF8:** El sistema debe permitir al ciudadano detallar el problema o sugerencia relacionado con el tipo seleccionado.

![Diagrama de casos de uso](/assets/Quejas%203.1asd.png)
![Diagrama de casos de uso](/assets/Quejas%203.1%20Confirmacionasd.png)

- **RF9:** El sistema debe mostrar al ciudadano el historial de quejas previas enviadas, incluyendo detalles como el asunto y una imagen asociada.

![Diagrama de casos de uso](/assets/Quejas%203.1asd-1.png)

- **RF10:** El sistema debe permitir al administrador revisar una lista de quejas o sugerencias recibidas, clasificadas por tipo de queja.

![Diagrama de casos de uso](/assets/Quejas%203.1asd-1.png)

- **RF11:** El sistema debe permitir al administrador modificar el estado de las quejas.

![Diagrama de casos de uso](/assets/Editar%20queja3.1/Adminasd.png)
![Diagrama de casos de uso](/assets/Editar%20queja3.1/Adminasd.png)
![Sondeos](./assets/Sondeosasd.png)

- **RF13:** El sistema debe permitir al ciudadano votar a favor o en contra de los proyectos mediante botones de "De acuerdo" o "Desacuerdo".

![Sondeos2](./assets/Sondeos%202asd.png) ![Sondeos3](./assets/Sondeos%20Confirmacionasd.png)

- **RF14:** El sistema debe permitir al administrador crear encuestas ingresando el título y el detalle o descripción del sondeo.

![Sondeos4](./assets/Realizar%20sondeo_admasd.png) ![Sondeos5](./assets/crear_sondeo_confirmasd.png)
 
- **RF15:** El sistema debe permitir al administrador consultar los resultados de las encuestas.

![Sondeos6](./assets/sondeo_mainasd.png) ![Sondeos7](./assets/sondeo_detalle_adminasd.png)

### 6. Acceso a Servicios de Emergencia
- **RF16:** El sistema debe permitir al ciudadano visualizar una lista de servicios de emergencia disponibles, como SAMU, PNP, Bomberos y Central de Serenazgo.

![SOS](./assets/SOSasd.png)

### 7. Configuración y Preferencias del Usuario

![Settings](./assets/Settingsasd.png)

- **RF17:** El sistema debe permitir al ciudadano activar o desactivar las notificaciones push desde la configuración.

![Settings2](./assets/Settings%20notificacionesasd.png)

- **RF18:** El sistema debe mostrar el nombre del usuario y permitirle agregar o actualizar su rostro para el inicio de sesión con identificación facial.

![Settings2.1](./assets/Identificador%20de%20rostro/validaciónasd.png)

![Settings2.2](./assets/Identificador%20de%20rostro/agregando%201asd.png) ![Settings2.3](./assets/Identificador%20de%20rostro/actualizadoasd.png)

![Settings2.4](./assets/Identificador%20de%20rostro/validación%20por%20emailasd.png) ![Settings2.5](./assets/Identificador%20de%20rostro/agregando%202asd.png) ![Settings2.1](./assets/Identificador%20de%20rostro/agregadoasd.png)

- **RF19:** El sistema debe permitir al ciudadano visualizar y gestionar los "Términos y condiciones".

![Settings3](./assets/Settings%20terminos%20y%20condicionesasd.png)

- **RF20:** El sistema debe permitir al ciudadano cerrar sesión desde la pantalla de ajustes.

![Settings](./assets/Settingsasd.png)

## Integrantes 👥
-Marcelo Cabrejos Benites (20200333)
-Renzo Tipula Cochachin (20202084)
-Roberto Lopez Jauregui (20201192)
-Arturo Aaron Silvera Pocco (20204965)
-Rafael Calderon (20200349)
