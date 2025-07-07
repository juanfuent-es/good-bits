# 🌱 Good Bits

---

## 🧠 Arquitectura y STACK Sugerido

### 🔍 Visión Computacional y Escaneo

| Funcionalidad                     | Tecnología Recomendada                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------|
| OCR para etiquetas               | [Google Cloud Vision OCR](https://cloud.google.com/vision/docs/ocr) / [Azure AI Vision OCR](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/overview) |
| Detección de logos y marcas      | [Google Cloud Logo Detection](https://cloud.google.com/vision/docs/detecting-logos)                     |
| Identificación de ingredientes   | [Google Vision Object Detection](https://cloud.google.com/vision/docs/object-localizer) / [Azure Vision](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/) |

---

### 🍽️ Recomendación de Recetas

#### 🔹 Opción rápida (MVP)
**Búsqueda de recetas desde servicios de terceros, usando ingredientes disponibles del usuario y coincidencias de ingredientes:**
- [Spoonacular API](https://spoonacular.com/food-api)  
- [Edamam API](https://developer.edamam.com/)

#### 🔹 Opción avanzada (NLP con Python)
**Generación de sistema de recomendación con IA (embeddings + clustering):**
- Proceso con implementación más lenta; mayor grado de complejidad
- Recolección de ~1000 recetas con curaduría manual
- Formato estructurado: ingredientes, pasos, cantidades, tags (vegano, árabe, etc.)
- Uso de modelos NLP con [spaCy](https://spacy.io/) / [Transformers](https://huggingface.co/transformers/)

---

### 📍 Mapas y Geolocalización

| Funcionalidad                  | Herramientas recomendadas                                                                 |
|-------------------------------|--------------------------------------------------------------------------------------------|
| Mapa de estaciones RVM        | [Google Maps SDK](https://developers.google.com/maps/documentation) / [Mapbox](https://www.mapbox.com/) |
| Alertas por proximidad (viajes) | [OneSignal](https://onesignal.com/) + GPS API con geofencing                              |

---

### ⚙️ Backend

- **Lenguaje/Framework**: [`Node.js`](https://nodejs.org/) con [`Express.js`](https://expressjs.com/) o [`NestJS`](https://nestjs.com/)
- **Base de Datos Relacional**: [`PostgreSQL`](https://www.postgresql.org/)
- **Autenticación**: [Firebase Auth](https://firebase.google.com/products/auth) o [Auth0](https://auth0.com/)
- **Arquitectura**: RESTful API con endpoints desacoplados y escalables (microservicios si es necesario)

### Flujo

[Input usuario (imagen JPG/PNG)] →
[API recibe archivo] →
[Preprocesamiento: resize, normalize, limpiar] →
[Modelo ejecuta inferencia] →
[Resultado JSON: ingrediente detectado, marca, cantidad] →
[Devuelve al frontend para sugerir recetas]


---

### 📢 Notificaciones

- **Push Notifications**: [OneSignal](https://onesignal.com/)
- **Email Marketing / Alertas**: [Mailjet](https://www.mailjet.com/)

---

### 🗂️ Almacenamiento y Procesamiento de Archivos

- **Almacenamiento**: [AWS S3](https://aws.amazon.com/s3/) o [Cloudinary](https://cloudinary.com/)
- **Procesamiento de imágenes**: [ImageMagick](https://imagemagick.org/)

---
