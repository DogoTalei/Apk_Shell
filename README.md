# Apk_Shell
📱 Android Reverse Shell (Java) Este proyecto es una APK de reproductor de video modificada que incluye una reverse shell escrita en Java puro, embebida directamente en el ciclo de vida de la aplicación (onCreate() de PlayerActivity). No requiere librerías externas ni root para ejecutarse.

🔧 Características
Reverse shell funcional usando Socket, InputStream y Runtime.exec("sh").

Conexión TCP saliente hacia un servidor de escucha (Serveo o VPS).

Comunicación bidireccional: permite enviar comandos y recibir resultados.

Integración discreta en una aplicación legítima (APK de reproductor de video).

Compatible con Android 6 a 13.

⚙️ Requisitos
Listener activo en el puerto especificado (nc -lvnp <puerto>).

Serveo, Ngrok o VPS configurado para recibir conexiones.

Android Studio o Gradle para compilar.

📁 Ruta de integración
Código de la reverse shell ubicado en ReverseShell.java.

Ejecutada desde PlayerActivity.java al iniciar la app.

🚨 Advertencia
Este proyecto es para uso educativo y de pruebas en entornos controlados. El uso indebido puede violar leyes locales o políticas de seguridad.



Comportamiento Sigiloso
Este proyecto está diseñado para ser altamente sigiloso y difícil de detectar tanto por el usuario como por soluciones de seguridad comunes. Aquí se explican sus propiedades evasivas:

🧬 Integración en Aplicación Real
La reverse shell está oculta dentro de una app legítima: un reproductor de video completamente funcional.

No crea iconos, notificaciones, ni actividades sospechosas visibles para el usuario.

Aprovecha el método onCreate() de PlayerActivity, lo que significa que la shell se inicia automáticamente al abrir la app, sin requerir interacción adicional.

🚫 Sin librerías externas
No usa herramientas o librerías de hacking conocidas (como msfvenom, Meterpreter, libcurl, etc.), lo que reduce la probabilidad de ser detectado por antivirus o EDR.

Está escrita solo en Java nativo y utiliza clases estándar del SDK de Android (Socket, InputStream, ProcessBuilder...), lo que simula el comportamiento de cualquier app común.

🔌 Comunicación Saliente
Establece una conexión saliente, lo cual es menos sospechoso desde el punto de vista de los firewalls y evita restricciones de NAT.

Esto permite evitar configuraciones complejas de puertos abiertos o root.

🛡️ Evasión de permisos
Aunque Android impone limitaciones desde la versión 6.0, esta shell solo necesita permisos básicos (INTERNET) que no generan alerta en el usuario.

Puede ampliarse para solicitar permisos sensibles de forma camuflada o programada si es necesario.
