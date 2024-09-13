# InLima - Grupo 4 🚀
## Entorno de desarrollo 💻
## Diagrama de despliegue 🌐
![Diagrama de despliegue](./mockups/d_despliegue.PNG)
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
![Diagrama de casos de uso](./mockups/d_casosdeuso.PNG)
## Descripción de casos de uso 📝

### Registrarse (Ciudadano)
#### Registrar cuenta
El usuario debe poder registrarse proporcionando correo, contraseña, DNI, nombre, apellidos y distrito actual

![registro](/assets/registrarseasd.png)
![confirmareg](/assets/registrarse%20Confirmaciónasd.png)
#### Registrar datos biometricos
El sistema debe permitir al usuario registrar o actualizar su rostro para usarlo como método de identificación, si el rostro no está registrado, el sistema debe solicitar al usuario que lo registre.

![agregando1](/assets/agregadoasd.png)
![agregando2](/assets/agregando%202asd.png)
![agregando3](/assets/validación%20por%20emailasd.png)
### Iniciar sesión
#### Iniciar sesión con credenciales

El sistema debe permitir al usuario iniciar sesión validando el correo y contraseña del usuario con la base de datos.
![agregando4](/assets/iniciar%20sesionasd.png)
![agregando5](/assets/Homeasd.png)
#### Iniciar sesión con datos biometricos

El sistema debe utilizar un identificador facial para permitir el inicio de sesión.
![agregando4](/assets/Iniciar%20sesion%20-%20Identificadorasd.png)
![agregando5](/assets/Iniciar%20sesion%20-%20Identificador%20Registroasd.png)

### Realizar queja (Ciudadano)
#### Seleccionar asunto
#### Completar datos

### Gestionar quejas (Administrador)
#### Consultar las quejas
#### Modificar el estado de las quejas

### Responder encuesta (Ciudadano)

### Gestionar encuestas (Administrador)
#### Crear encuesta
#### Consultar resultados

### Llamar a emergencias (Ciudadano)

### Configurar notificaciones

## Integrantes 👥
