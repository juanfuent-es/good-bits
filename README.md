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

- **Lenguaje/Framework**: [`Python`](https://www.python.org/) con [`Flask`](https://flask.palletsprojects.com/) (ligero, ideal para MVPs) o [`Django`](https://www.djangoproject.com/) (más estructurado y completo)
- **Base de Datos Relacional**: [`PostgreSQL`](https://www.postgresql.org/)
- **Autenticación**:
  - Con Django: Sistema de autenticación integrado + soporte para OAuth y JWT ([Django AllAuth](https://django-allauth.readthedocs.io/en/latest/), [Django Rest Framework SimpleJWT](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/))
  - Con Flask: [Flask-JWT-Extended](https://flask-jwt-extended.readthedocs.io/en/stable/) o integración con [Authlib](https://docs.authlib.org/)
- **Arquitectura**: RESTful API desacoplada usando [Django REST Framework](https://www.django-rest-framework.org/) o [Flask-RESTful](https://flask-restful.readthedocs.io/).  
  Escalable con posibilidad de adoptar microservicios (e.g. Flask Blueprint, Django Apps)


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
