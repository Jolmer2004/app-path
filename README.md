# app-path

Laboratorio Pipelines — Arquitectura de Software (UCEVA).
Aplicación Angular con **Path Location Strategy** desplegada en GitHub Pages mediante GitHub Actions.

## Vistas
- `/` Inicio
- `/about` Acerca de
- `/contact` Contacto

Ejemplo de URL: `https://USUARIO.github.io/app-path/about`

## Despliegue
1. Crear un repositorio **público** en GitHub llamado `app-path` (el nombre debe coincidir con el `--base-href`, que el workflow toma de `github.event.repository.name`).
2. En **Settings → Pages → Source** seleccionar **GitHub Actions**.
3. Hacer push a `main` o `master`; el pipeline (`.github/workflows/deploy.yml`) instala, prueba, compila y publica.

El workflow copia `index.html` a `404.html` para que el acceso directo a rutas (por ejemplo `/app-path/about`) funcione en GitHub Pages.

## Comandos
```bash
npm install
npm start        # desarrollo
npm test         # pruebas unitarias
npm run build    # build de producción
```
