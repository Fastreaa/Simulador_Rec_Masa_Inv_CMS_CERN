# Simulador de Masa Invariante — CMS Open Data (CERN)

Simulador visual e interactivo de reconstrucción de masa invariante de eventos dimuón, construido sobre datos reales y públicos del experimento **CMS** del **CERN** (CMS Open Data, record 5201, *"Dimuon_DoubleMu.csv"*).

Reproduce, evento a evento y en el navegador, el mismo flujo de análisis de un notebook académico (carga total del par, filtro de candidatos neutros, cálculo de M² y M, histograma acumulado con ajuste señal + fondo) sincronizado con una representación 3D esquemática del detector CMS, incluyendo una vista de corte que deja un lado abierto para seguir las trayectorias de los muones sin obstrucciones.


## Qué incluye

- **Simulador** — carga de CSV (archivo local o URL), reproducción evento por evento con animación 3D, histograma en vivo con bandas de color por resonancia conocida (ω/φ, J/ψ, ψ′, Υ, Z⁰) y ajuste gaussiana + fondo lineal.
- **Código puro (Python)** — el mismo análisis corriendo de verdad en el navegador vía Pyodide (numpy, pandas, scipy, matplotlib), con fragmentos de código listos para ejecutar y editar.
- **Panel educativo** — contexto sobre el CERN, el experimento CMS, qué es un muon, por qué se usan dimuones para reconstruir masa, y por qué este mismo método se usa para buscar partículas nuevas (incluido el descubrimiento del Higgs en 2012).
- **Modelo 3D del detector** — geometría inspirada en el diagrama técnico oficial "CMS DETECTOR" (tracker, calorímetros, solenoide, yugo de retorno, cámaras de muones, calorímetro frontal), con vista de corte (cutaway) en un lado.

## Fuente de datos

CMS Open Data, record 5201 ("Dimuon_DoubleMu.csv"), publicado por el CERN. El archivo incluye un botón de carga por URL con un espejo verificado del mismo dataset en el repositorio educativo [`cms-opendata-education`](https://github.com/cms-opendata-education/cms-jupyter-materials-english) de GitHub.

## Cómo usarlo

Es un único archivo HTML autocontenido (`index.html`). Solo necesitas abrirlo en un navegador moderno con conexión a internet (para cargar las librerías por CDN: Three.js, Chart.js, PapaParse, KaTeX y, bajo demanda, Pyodide). No requiere instalación ni servidor.

Todas las simplificaciones y decisiones técnicas están documentadas de forma honesta en el comentario al inicio del propio archivo `index.html` (qué es esquemático, qué se verificó, y qué limitaciones conocidas existen).

## Créditos

Basado en el notebook educativo *"MasaInvariante — análisis de datos del CMS utilizando ROOT y Python"* y en los datos abiertos del CERN/CMS.
