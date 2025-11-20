<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>TECGameScraper README</title>
<style>
    body {
        font-family: Arial, sans-serif;
        max-width: 900px;
        margin: 40px auto;
        padding: 20px;
        line-height: 1.6;
        background: #0b1120;
        color: #e5e7eb;
    }
    h1, h2, h3 {
        color: #22c55e;
    }
    .box {
        padding: 15px;
        background: #111827;
        border-left: 4px solid #22c55e;
        margin: 15px 0;
        border-radius: 8px;
    }
    a { color: #60a5fa; }
</style>
</head>
<body>

<h1>🎮 TECGameScraper</h1>
<h3>Scraping de Ofertas de Videojuegos · Multiproceso · Firebase · Dashboard Web</h3>

<p>
<b>TECGameScraper</b> es un proyecto creado por <b>estudiantes de primer año del TEC | San Carlos</b>.  
El objetivo fue construir un sistema real que combina scraping, procesamiento inteligente de datos y una visualización web moderna.
</p>

<h2>✨ ¿Qué hace este proyecto?</h2>

<div class="box">
<ul>
    <li>🔎 Scrapea información de videojuegos desde Steam, Amazon, HowLongToBeat y Metacritic.</li>
    <li>⚙️ Procesa todo en paralelo (async + multiproceso).</li>
    <li>📦 Genera un JSON con precios, tiempos y ratings.</li>
    <li>☁️ Lo sube automáticamente a Firebase Realtime Database.</li>
    <li>🖥️ Muestra todo en un dashboard web oscuro, moderno y filtrable.</li>
</ul>
</div>

<h2>🧱 Tecnologías Utilizadas</h2>

<h3>🔵 Backend (Python)</h3>
<ul>
<li>aiohttp – Requests asíncronos</li>
<li>asyncio – Concurrencia</li>
<li>ProcessPoolExecutor – Multiproceso real</li>
<li>BeautifulSoup – Parsing HTML</li>
<li>tenacity – Retries inteligentes</li>
<li>firebase-admin – Envío a Firebase</li>
</ul>

<h3>🟢 Base de Datos</h3>
<p><b>Firebase Realtime Database</b></p>
<p>Ruta: <code>/scraping/resultados_juegos</code></p>

<h3>🟣 Frontend</h3>
<ul>
<li>HTML + CSS + JavaScript Vanilla</li>
<li>Dashboard tipo "dark mode"</li>
<li>Tarjetas dinámicas, filtros, modal de detalles</li>
</ul>

<h2>🎓 Sobre Nosotros</h2>
<p>
Somos estudiantes del <b>Tecnológico de Costa Rica</b> que estamos aprendiendo tecnologías reales desde primer año.  
Este proyecto nos enseñó scraping, concurrencia, bases en la nube y diseño web moderno.
</p>

</body>
</html>
