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
El ciudadano podrá registrarse blablabla

![Login](./mockups/login.PNG)
#### Registrar datos biometricos

### Iniciar sesión
#### Iniciar sesión con credenciales
#### Iniciar sesión con datos biometricos

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
