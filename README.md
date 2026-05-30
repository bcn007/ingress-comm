# Analiticgress2 V2

Paquete limpio para entregar o subir a GitHub.

## Contenido

- `index.html`: ultima version movil-first lista para GitHub Pages.
- `.github/workflows/cook.yml`: automatizacion nocturna de GitHub Actions.
- `.gitignore`: evita subir logs crudos, cache y archivos temporales.
- `cooker/cook.py`: cocina los JSON brutos y genera datos estaticos.
- `cooker/sync_drive.py`: descarga JSONs desde Google Drive.
- `cooker/requirements.txt`: dependencias Python.
- `cooker/README.md`: instrucciones del cooker.
- `cooker/ARCHITECTURE_V3.md`: plan tecnico de arquitectura.

## No incluido

- No incluye `cooker/raw/`.
- No incluye claves ni secrets.
- No incluye `GOOGLE_SERVICE_ACCOUNT_JSON`.
- No incluye `GOOGLE_DRIVE_SOURCE_FOLDER_ID`.

## Secrets necesarios en GitHub

En `Settings > Secrets and variables > Actions > Repository secrets`:

- `GOOGLE_SERVICE_ACCOUNT_JSON`
- `GOOGLE_DRIVE_SOURCE_FOLDER_ID`

## Publicacion

Subir el contenido de esta carpeta a la raiz del repo.

La web final queda en:

`https://bcn007.github.io/Analiticgress2/`

El workflow se puede lanzar manualmente desde:

`Actions > Cook Ingress data > Run workflow`

Tambien se ejecuta automaticamente cada noche segun `.github/workflows/cook.yml`.

