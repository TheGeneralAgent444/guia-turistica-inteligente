# Guía Turística Inteligente con IA y Geolocalización  
## Arquitectura Modular y Diseño por Capas  

**Fundación Universitaria Lumen Gentium (UNICATÓLICA)**  
**Asignatura:** Desarrollo de Software I  
**Docente:** Stephany Ramírez Posada  
**Integrantes:**  
- Luisa Gironza Beltrán (ID: 408993)  
- Jose Luis Hoyos Salazar (ID: 408716)  

---

### Propósito del Documento
Este documento describe la **arquitectura modular y diseño por capas** del sistema “Guía Turística Inteligente con IA y Geolocalización”.  
El objetivo es dividir el sistema en módulos funcionales y definir la interacción entre ellos, aplicando los principios de arquitectura modular.

---

## 1. Módulos Funcionales

| Módulo | Funcionalidad | Descripción |
|--------|----------------|-------------|
| **Gestión de usuarios** | Registro e inicio de sesión | Control de autenticación, perfiles, idiomas y accesibilidad. |
| **Recomendaciones inteligentes (IA)** | Sugerencias personalizadas | Aplica algoritmos de machine learning según preferencias e historial. |
| **Itinerarios dinámicos** | Planificación de viajes | Genera rutas adaptadas al clima, tráfico y horario. |
| **Geolocalización** | Mapa y ubicaciones | Usa APIs (Google Maps, Mapbox) para mostrar lugares cercanos. |
| **Notificaciones inteligentes** | Alertas automáticas | Envía recordatorios sobre eventos o clima. |
| **Gestión de reseñas** | Opiniones de usuarios | Permite calificar y comentar lugares visitados. |

---

## 2. Arquitectura por Capas

El sistema sigue una **arquitectura de tres capas**:

1. **Capa de Presentación (Frontend)**  
   - Interfaz móvil intuitiva.  
   - Permite interacción directa con el usuario.  
   - Tecnologías: Flutter / React Native / Kotlin.  

2. **Capa de Lógica de Negocio (Backend)**  
   - Contiene la lógica de recomendaciones, itinerarios y validaciones.  
   - Conecta la app con los servicios externos (APIs de mapas, clima, IA).  
   - Lenguaje sugerido: Python (FastAPI) o Node.js.  

3. **Capa de Datos (Base de Datos)**  
   - Almacena información de usuarios, lugares, reseñas e itinerarios.  
   - Base de datos relacional (MySQL / PostgreSQL).  

---

## 3. Diagrama de Arquitectura (Esquema)

