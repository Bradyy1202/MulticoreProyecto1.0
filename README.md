# 🎮 TECGameScraper  
### Scraping de Ofertas de Videojuegos · Multiproceso · Firebase · Dashboard Web

**GameScraper** es un proyecto creado por nosotros **estudiantes de primer año del TEC | San Carlos**.  
Nace como un reto para construir desde cero un sistema real que combine scraping, procesamiento inteligente de datos y visualización web moderna.

---

## ✨ ¿Qué hace este proyecto?

🔎 **Scrapea información de videojuegos** desde múltiples sitios:  
- Steam  
- Amazon  
- HowLongToBeat  
- Metacritic  

⚙️ **Procesa todo en paralelo** (async + multiproceso) para hacerlo súper rápido.  
📦 **Genera un JSON completo** con precios, tiempos de juego, ratings y metadatos.  
☁️ **Lo sube automáticamente a Firebase Realtime Database**.  
🖥️ **Lo muestra en un dashboard web elegante**, filtrable y con tarjetas interactivas.

En resumen:  
👉 Es un **motor de ofertas** hecho completamente por estudiantes, con herramientas reales de la industria.

---

## 🧱 Tecnologías Utilizadas

### 🔵 Backend (Python)
- `aiohttp` – Requests asíncronos  
- `asyncio` – Concurrencia  
- `ProcessPoolExecutor` – Multiproceso real  
- `BeautifulSoup` – Parsing HTML  
- `tenacity` – Retries inteligentes  
- `firebase-admin` – Envío a Realtime Database  

### 🟢 Base de Datos
- **Firebase Realtime Database**  
  Ruta donde se guarda todo:  
  `/scraping/resultados_juegos`

### 🟣 Frontend
- HTML + CSS + JavaScript Vanilla  
- Diseño tipo **dashboard oscuro**, moderno y limpio  
- Tarjetas dinámicas, filtros y modal de detalles  

---


