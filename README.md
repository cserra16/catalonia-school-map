# Mapa de Centres Educatius de Catalunya

Aplicació web interactiva que mostra els centres educatius de Catalunya en un mapa, amb opcions de filtratge per nivell educatiu, ubicació i titularitat del centre.

## Característiques

- Visualització de centres educatius en un mapa interactiu
- Filtratge per:
  - Nivell educatiu (Infantil, Primària, ESO, Batxillerat, FP)
  - Municipi
  - Codi postal
  - Titularitat (Públic, Concertat, Privat)
- Cerca per nom de centre
- Informació detallada de cada centre en fer clic al marcador

## Requisits

- Navegador web modern (Chrome, Firefox, Safari, Edge)
- Connexió a Internet (per carregar Google Maps API)

## Instal·lació

1. Clona el repositori:
   ```bash
   git clone https://github.com/tu-usuario/catalonia-school-map.git
   cd catalonia-school-map
   ```

2. Configura l'API de Google Maps:
   - Crea un fitxer `js/config.js` basat en l'exemple:
     ```bash
     cp js/config.example.js js/config.js
     ```
   - Obté una API key des de [Google Cloud Console](https://console.cloud.google.com/)
   - Reemplaça `'TU_API_KEY_AQUI'` a `js/config.js` amb la teva API key

3. Serveix els fitxers a través d'un servidor web local:
   ```bash
   # Python 3
   python -m http.server 8000
   ```

4. Obre el navegador a `http://localhost:8000`

## Estructura del Projecte

- `index.html` - Pàgina principal de l'aplicació
- `csv/` - Directori amb les dades dels centres educatius
  - `centres-educatius_utf8.csv` - Dades dels centres en format UTF-8
- `README.md` - Aquest fitxer
- `.gitignore` - Fitxer de configuració de Git

## Llicència

Aquest projecte està sota la Llicència MIT. Consulta el fitxer `LICENSE` per a més detalls.

## Dades

Les dades dels centres educatius són proporcionades pel Departament d'Educació de la Generalitat de Catalunya.

## Contribucions

Les contribucions són benvingudes. Si us plau, crea un issue per discutir els canvis proposats abans de fer un pull request.
