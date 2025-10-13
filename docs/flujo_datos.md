# Guía Turística Inteligente con IA y Geolocalización
## Actividad 2 – Flujos de Información y Estructuras de Datos

**Fundación Universitaria Lumen Gentium (UNICATÓLICA)**  
**Asignatura:** Desarrollo de Software I  
**Docente:** Stephany Ramírez Posada  
**Integrantes:**  
- Luisa Gironza Beltrán (ID: 408993)  
- Jose Luis Hoyos Salazar (ID: 408716)  

---

### Propósito del Documento
El propósito de este documento es describir **cómo viajan los datos entre las capas** de la aplicación y **qué estructuras de datos** emplea cada módulo para garantizar eficiencia, escalabilidad y organización.

---

## 1. Diagrama de Flujo de Información

El sistema está basado en una **arquitectura de tres capas (Presentación, Negocio y Datos)**.  
El flujo general de la información se da de la siguiente forma:
[Usuario]
↓
[Capa de Presentación]
↓
[Controlador / API]
↓
[Capa de Lógica de Negocio]
↓
[Capa de Datos (Base de datos)]
↓
[Respuesta al usuario]

- **Capa de Presentación (App móvil):**  
  Recibe entradas del usuario (preferencias, ubicación, idioma).  

- **Capa de Lógica de Negocio:**  
  Procesa los datos, aplica los algoritmos de IA, genera recomendaciones y actualiza itinerarios.  

- **Capa de Datos:**  
  Almacena la información persistente (usuarios, lugares, reseñas, itinerarios, notificaciones).  

---

## 2. Estructuras de Datos por Módulo

| Módulo | Tipo de estructura | Ejemplo / uso | Descripción |
|---------|--------------------|----------------|--------------|
| **Gestión de Usuarios** | Registro (diccionario / JSON) | `{id, nombre, email, idioma, historial}` | Almacena la información personal y preferencias del usuario. |
| **Geolocalización** | Tuplas o listas de coordenadas | `[(lat, lon), (lat, lon)]` | Guarda la ubicación actual y los puntos turísticos cercanos. |
| **Recomendaciones con IA** | Lista o árbol de decisión | `[lugares_recomendados]` | Contiene los destinos generados según el historial y gustos. |
| **Itinerarios Dinámicos** | Lista enlazada / árbol | `Día1 → Día2 → Día3` | Ordena las actividades y permite agregar o eliminar destinos. |
| **Notificaciones** | Cola (FIFO) | `[not1, not2, not3...]` | Gestiona el envío de alertas en tiempo real. |
| **Reseñas** | Lista de objetos | `[ {usuario, destino, calificación, comentario}, ... ]` | Almacena las reseñas creadas por los usuarios. |

---

## 3. Ejemplo de Flujo Completo

1. El usuario solicita **“destinos turísticos cercanos”** desde la app.  
2. La **Capa de Presentación** envía la solicitud (ubicación actual) al **backend**.  
3. La **Capa de Lógica de Negocio** consulta en la base de datos los lugares disponibles.  
4. El módulo de **IA** filtra los resultados según preferencias del usuario.  
5. El sistema devuelve al usuario una lista de recomendaciones y actualiza su historial.  

---

## 4. Diagrama Visual del Flujo de Datos

A continuación se presenta el diagrama general de flujo:

![Diagrama de Flujo de Información](../interfaces/flujo_datos.drawio.png)

*(El diagrama representa la interacción de las tres capas y los módulos funcionales del sistema).*

---

## 5. Conclusión

El flujo de información permite una comunicación eficiente entre las capas del sistema.  
El uso de estructuras de datos como **listas, árboles, colas y registros** asegura que los procesos sean rápidos, organizados y adaptables al crecimiento del sistema.

---
