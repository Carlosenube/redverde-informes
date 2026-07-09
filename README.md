# Informes de campaña

Informes mensuales de campañas (Google Ads, etc.) servidos como estáticos en Vercel,
con una URL por informe.

## Convención de carpetas

```
<cliente>/<mes-año>/index.html
```

- **`<cliente>`** — slug en minúsculas y sin espacios del cliente (ej. `redverde`).
- **`<mes-año>`** — mes y año en minúsculas separados por guion (ej. `julio-2026`).
- **`index.html`** — el informe en sí. Un único HTML autocontenido por carpeta.

Cada carpeta se sirve en su propia ruta. Por ejemplo:

```
redverde/julio-2026/index.html   →   https://<dominio>/redverde/julio-2026/
```

## Añadir un informe nuevo

1. Crea la carpeta siguiendo la convención: `<cliente>/<mes-año>/`.
2. Coloca dentro el `index.html`.
3. Commit y push — Vercel despliega automáticamente al detectar el nuevo commit.

## Despliegue

Estático puro, sin paso de build (ver [`vercel.json`](vercel.json)).
