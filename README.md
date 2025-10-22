# BUS Gijón — Interfaz de consulta de llegadas (EMTUSA)

Este repositorio contiene una página estática (`index.html`) que proporciona una interfaz sencilla para consultar las próximas llegadas de autobuses de EMTUSA (Gijón) para una parada concreta, buscar paradas y gestionar una lista de favoritas.

## Qué hace `index.html`

- Carga la lista completa de paradas disponibles y permite buscar por nombre o por ID.
- Muestra la información detallada de una parada: descripción, ID y próximas llegadas (línea, destino, minutos estimados, distancia y tiempo desde la última posición GPS).
- Permite marcar / desmarcar paradas como favoritas y almacenarlas en `localStorage` del navegador. Las favoritas se muestran en un dropdown y se pueden eliminar.
- Actualiza automáticamente la información de la parada seleccionada cada 30 segundos y muestra un temporizador que indica cuándo se actualizó por última vez.
- Interfaz responsiva y con estilos basados en Bootstrap 5 y Bootstrap Icons.

## Cómo probar localmente

1. Clona o descarga este directorio en tu máquina.
2. Abre `index.html` en un navegador moderno (Chrome, Firefox, Edge). Idealmente sirve el archivo mediante un servidor local (por ejemplo `python -m http.server`) para evitar posibles restricciones de CORS o comportamientos al abrir archivos locales.

Ejemplo rápido con Python (desde la carpeta `emtusa_web`):

```bash
# en Linux/macOS
python3 -m http.server 8000
# luego abre http://localhost:8000 en tu navegador
```

## Despliegue

Ya que toda la funcionalidad se ejecuta en el navegador, puedes desplegar `index.html` en cualquier servidor web estático (GitHub Pages, Netlify, Vercel, etc.) sin necesidad de backend adicional.

En un móvil o tablet basta apuntar a la URL donde esté alojado el archivo estático. Una vez se ve la página, se puede también añadir a la pantalla de inicio para un acceso más rápido.


## Licencia y créditos

Este repositorio es solo una interfaz de cliente para la API pública de EMTUSA. Reutiliza iconos y estilos de Bootstrap y Bootstrap Icons (CDN). Comprueba las licencias de terceros si planeas redistribuir.

