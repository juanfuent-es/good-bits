**DESARROLLO / QA**  
**$12–18 USD/mes** – *DigitalOcean Droplet*  
Servidor temporal para el desarrollo del Backend for Frontend (Ruby on Rails + API REST).

**~$5 USD/mes** – *DigitalOcean Spaces*  
Almacenamiento de imágenes y archivos del usuario. Incluye 250 GB y 1 TB de transferencia mensual.

> **Nota:** Estos servicios serán únicamente para la etapa de desarrollo; una vez liberada la PWA, el hosting se migrará a AWS y el costo será absorbido por el cliente. Ya se comentó que el cliente cuenta con esta plataforma para desarrollo; solo será necesario que nos proporcione acceso para el montaje y la configuración.

---

**$15 USD/mes** – *SendGrid* o *Mailjet* (plan básico para 10 000 emails/mes)  
Envío de correos transaccionales (registro, recuperación de contraseña) y, opcionalmente, correos promocionales.

---

**$0 USD** – *OneSignal* (plan gratuito hasta 30 000 suscriptores y 100 segmentos)  
Push Notifications:  
- Requiere que el usuario instale la PWA en su pantalla de inicio para habilitar notificaciones.  
- Para usuarios iOS, se requiere sistema actualizado a partir de la versión 16.4.  
- La función de notificación por proximidad requiere las coordenadas (latitud y longitud) de todas las máquinas.  
- En la PWA del MVP, el geofencing se implementa de forma simulada mediante intervalos que calculan la cercanía, con mayor éxito y precisión mientras la aplicación esté activa en el teléfono del usuario.  
- El geofencing persistente en segundo plano solo es posible en aplicaciones nativas.

---

**~$5–15 USD/mes** – *Mapbox* (o Google Maps SDK)  
Mapas interactivos y geolocalización para mostrar estaciones y alertas. Plan gratuito hasta 50 000 visualizaciones mensuales; con un uso más intensivo, el gasto estimado puede subir a 15 USD/mes.

---

**$25–40 USD/mes** – *OpenAI API* (gpt-4o-mini)  
Procesamiento de imágenes y generación de recetas personalizadas con IA. Estimado para 10 000 usuarios mensuales, considerando margen para prompts y respuestas más extensas.

---

**Rango estimado mensual total:**  
**Entre $62 y $93 USD**
