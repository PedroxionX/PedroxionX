# Perfil y CV

Este repositorio reúne el perfil de GitHub y el CV público:

- `README.md`: perfil mostrado en github.com/PedroxionX.
- `site/index.html`: CV, con estilos y contenido en un único archivo estático.
- `.github/workflows/pages.yml`: validación y publicación automática.

El CV se importó desde `PedroxionX/Resume`, commit `0d10f58`, incluyendo la publicación de MexIHC 2026 y ORCID. No requiere Node, dependencias ni compilación.

## Edición y vista previa

Edita `site/index.html`. Para probarlo localmente, desde la raíz:

```sh
python3 -m http.server 8000 --directory site
```

Abre http://localhost:8000. El CV conserva los estilos de impresión del original.

## Publicación

GitHub Pages debe usar **GitHub Actions** como fuente en Settings → Pages.
Cada push a `main` que modifique `site/` o el workflow publica el CV en:

https://pedroxionx.github.io/PedroxionX/

Los pull requests validan y empaquetan el sitio sin publicarlo. También se puede ejecutar el workflow manualmente desde Actions. Solo se publica `site/`; la documentación y el perfil quedan fuera del sitio.

El repositorio `Resume` queda como redirección de compatibilidad para enlaces antiguos. Todo cambio futuro al CV se hace aquí. Su historial original se conserva en ese repositorio.
