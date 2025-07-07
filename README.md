# Good Bits

## 🧠 Arquitectura y STACK sugerido

### 🔍 Visión Computacional y Escaneo

|--------------------------------|--------------------------------------------------|
| Uso                            | Tecnología Recomendada                           |
|--------------------------------|--------------------------------------------------|
| OCR para etiquetas             | Google Cloud Vision OCR / Azure AI Vision        |
| Detección de logos y marcas    | Google Cloud Logo Detection                      |
| Identificación de ingredientes | Google Vision Object Detection / Azure Vision    |
|--------------------------------|--------------------------------------------------|

### 🍽️ Recomendación de Recetas

RECOMENDACIÓN E IMPLEMENTACIÓN MÁS RÁPIDA:
Buscar recetas (alimentadas desde servicios de terceros) que contengan ingredientes del usuario

- **APIs externas**:  
  - [Spoonacular API](https://spoonacular.com/food-api)  
  - [Edamam API](https://developer.edamam.com/)

IMPLEMENTACIÓN MÁS LENTA CON NIVEL TÉCNICO MÁS COMPLEJO (Python + )
Generación de modelo IA para embeddings semánticos y clustering para sugerencias similares.

Consideraciones:
Recoleccción media de 1000 recetas con curaduría manual
Guardar formato estructurado: ingredientes, pasos, cantidades, taggings, categorización (vegano, árabe, etc.)

---

### 📍 Mapas y Geolocalización

- **Mapa de estaciones RVM**: Google Maps SDK / Mapbox  
- **Alertas por proximidad**: Geofencing con OneSignal + GPS API

---

### Backend

- **Lenguaje/Framework**: `Node.js` con `Express.js` o `NestJS`
- **Base de Datos Relacional**: `PostgreSQL`
- **Autenticación y flujo de usuario**
- **API REST** modularidad con endpoints de microservicios escalables

---

### Notificaciones

- **Push Notifications**: OneSignal  
- **Email marketing / recordatorios**: Mailjet (opcional)

---

### Almacenamiento de Archivos

- AWS S3, Cloudinary, ImageMagick para procesamiento y optimización

---

### 🖥️ Hosting - Servidor Recomendado
**DigitalOcean Droplet | AWS EC2 / Lambda**

|-----------------|-------------------------------------------|
| Recurso         | Especificación mínima recomendada         |
|-----------------|-------------------------------------------|
| CPU             | 2 vCPUs                                   |
| RAM             | 4–8 GB                                    |
| Almacenamiento  | 50 GB SSD (escalable según imágenes)      |
| SO              | Ubuntu 22.04 LTS                          |
| Base de datos   | PostgreSQL (servidor gestionado)          |
| Seguridad       | HTTPS + JWT + backups + monitorización    |
|-----------------|-------------------------------------------|

## 📌 Consideraciones

- Validación inicial de OCR con dataset local de productos en Omán.
- Backend desacoplado de frontend para facilitar futuras extensiones.

---
