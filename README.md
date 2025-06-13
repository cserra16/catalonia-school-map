# Mapa de Centros Educativos de Cataluña

Aplicación web interactiva que muestra los centros educativos de Cataluña en un mapa, con opciones de filtrado por nivel educativo, ubicación y titularidad del centro.

## Características

- Visualización de centros educativos en un mapa interactivo
- Filtrado por:
  - Nivel educativo (Infantil, Primaria, ESO, Bachillerato, FP)
  - Municipio
  - Código postal
  - Titularidad (Público, Concertado, Privado)
- Búsqueda por nombre de centro
- Información detallada de cada centro al hacer clic en el marcador

## Requisitos

- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Conexión a Internet (para cargar Google Maps API)

## Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/catalonia-school-map.git
   cd catalonia-school-map
   ```

2. Configura la API de Google Maps:
   - Crea un archivo `js/config.js` basado en el ejemplo:
     ```bash
     cp js/config.example.js js/config.js
     ```
   - Obtén una API key de [Google Cloud Console](https://console.cloud.google.com/)
   - Reemplaza `'TU_API_KEY_AQUI'` en `js/config.js` con tu API key

3. Sirve los archivos a través de un servidor web local:
   ```bash
   # Python 3
   python -m http.server 8000
   ```

4. Abre tu navegador en `http://localhost:8000`

## Estructura del Proyecto

- `index.html` - Página principal de la aplicación
- `csv/` - Directorio con los datos de los centros educativos
  - `centres-educatius_utf8.csv` - Datos de los centros en formato UTF-8
- `README.md` - Este archivo
- `.gitignore` - Archivo de configuración de Git

## Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## Datos

Los datos de los centros educativos son proporcionados por el Departament d'Educació de la Generalitat de Catalunya.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, crea un issue para discutir los cambios propuestos antes de hacer un pull request.

## Cybersecurity Best Practices

### Google Maps API Key Security

To protect your Google Maps API key and prevent unauthorized use, follow these best practices:

1.  **Keep `js/config.js` private:** Never commit your `js/config.js` file (which contains your API key) to version control. The `.gitignore` file in this project is already configured to help prevent this, but always double-check.
2.  **Restrict your API key in the Google Cloud Console:**
    *   **By HTTP referrer:** Restrict your key to your specific domain (e.g., `*.yourdomain.com/*`). This prevents others from using your key on their websites.
    *   **To only the "Maps JavaScript API":** Limit the key's usage to only the necessary API. This prevents it from being used for other Google Cloud services you might not intend.

Following these steps helps prevent unauthorized use of your key on other websites or for other services, which could lead to unexpected charges or quota issues.
