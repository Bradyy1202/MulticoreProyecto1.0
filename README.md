# MulticoreProyecto1.0

hazlo mas sencillo y mas bonito visualmente

# 🎮 TECGameScraper  
### Motor de Ofertas de Videojuegos – Scraping Asíncrono + Multiproceso + Firebase

Este proyecto es desarrollado por **estudiantes de primer año del Tecnológico de Costa Rica (TEC)** como parte de nuestra formación inicial en programación, arquitectura de software y construcción de herramientas tecnológicas reales.  

Nuestro objetivo fue llevar un proyecto “de verdad” desde cero hasta un prototipo funcional que reúne:  
✔ Web Scraping  
✔ Concurrencia (async/await)  
✔ Multiproceso  
✔ Bases de datos en la nube  
✔ Visualización web interactiva  

Todo en un solo ecosistema.

---

## 🧩 Descripción del Proyecto

**TECGameScraper** es un sistema completo que:
1. Realiza web scraping masivo de videojuegos desde varias tiendas y sitios de referencia.  
2. Procesa toda la información de manera paralela (asíncrona + multiproceso) para maximizar velocidad.  
3. Construye un JSON estructurado con precios, tiempos de juego, calificaciones y metadatos.  
4. Sube el resultado automáticamente a **Firebase Realtime Database**.  
5. Alimenta un **frontend web tipo dashboard**, moderno y fluido, que permite filtrar, ordenar y explorar cada título de forma visual.

Es, básicamente, un **motor de ofertas**, pero hecho completamente desde cero por estudiantes.

---

## 🏗 Arquitectura General

### 🟦 1. Backend en Python  
Archivo principal: `WebScrappingParalelism.py`

Incluye:

- **Scraping Asíncrono**  
  - `aiohttp` para realizar múltiples requests simultáneamente.  
  - `asyncio.Semaphore` para limitar concurrencia.  
- **Multiproceso**  
  - `ProcessPoolExecutor` divide el procesamiento de 200 juegos entre varios procesos.  
- **Web Scraping Inteligente**
  - **Steam API** (búsqueda + detalles)  
  - **Amazon** (categoría videojuegos, filtrado de precios reales)  
  - **HowLongToBeat** (HLTB)  
    - Con fallback determinístico si falla  
  - **Metacritic** (búsqueda HTML + fallback)  
- **Procesamiento de datos**
  - Elección de la mejor tienda según precio.  
  - Identificación automática de plataforma, tipo (Digital/Físico/Mixto) y descuento simulado.  

- **Integración con Firebase Realtime Database**  
  Se sube el payload completo a:  
  `/scraping/resultados_juegos`

- **Modo automático**
  ```bash
  python WebScrappingParalelism.py --continuous
