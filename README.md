# Climaire

Sitio web de Climaire. Build estático (Vite + React) desplegado en **GitHub Pages**.

Anteriormente se servía dentro de [`alannabricks-web`](https://github.com/alannabricks/alannabricks-web)
en la ruta `/cliente/climaire/`. Al quedar aprobado se movió a su propio
repositorio para tener ciclo de vida y deploy independientes.

## Contenido

- `index.html` — punto de entrada (rutas de assets relativas: `./assets/...`).
- `assets/` — bundle JS y CSS compilado.
- `favicon.svg`
- `.github/workflows/deploy-pages.yml` — publica el sitio en GitHub Pages en cada push a `main`.

> **Nota:** este repo contiene únicamente el **artefacto compilado**. El código
> fuente (proyecto Vite con `src/config/seo.ts`, etc.) no está incluido. Para
> regenerar el build hay que partir del proyecto fuente original.

## Deploy

El workflow toma los archivos estáticos, los pone en `_site/` (con `.nojekyll`)
y los publica vía `actions/deploy-pages`. URL por defecto:

```
https://alannabricks.github.io/climaire-web/
```

Si más adelante se usa un dominio propio (p. ej. `climaire.cl`), agregar un
archivo `CNAME` con el dominio y actualizar el string `domain` del bundle.
