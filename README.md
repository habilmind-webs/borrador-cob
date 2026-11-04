# Borrador · COB (Cuestionario de Orientación al Bachillerato)

Borrador pedido por Rosario (vía Doña Clotilde) el 04/11/2026. **Solo staging**: https://borrador-cob.2-31-95-201.sslip.io (noindex). Sin dominio real ni DNS: eso solo con el OK de Joaquín. **COB es solo para España.**

- Diseño = borrador-cai (@735773b): mismo `src/style.css`, `src/cookies.js`, `src/expertos.js`, `src/main.js`, header sticky, hamburguesa, «Más», ficha técnica tipo socioemociograma, cierre tipo socio, pie, banner Flash y chat de Ofelia. Solo se añaden al final de `style.css` unos ajustes marcados «COB».
- Copy literal del brief de Rosario (`webs:/tmp/dc-share/cob-borrador-BRIEF.md`). Generador fuera del repo: `/workspace/cob/gen.py` (box de Esmarelda).
- Nav = socioemociograma sin Fundamentación (como CAI): Qué es, Aplicación, Indicadores, Informes, Más (Videos, Preguntas frecuentes, Infografía, Tour guiado), Soporte, Reunión o llamada (CTA Ofelia `cob`), Precios.
- Multipágina con Vite; la home redirige `/slug` y `/slug/` a `/slug/index.html` (el staging usa `import spa`) y la subpágina limpia la URL. Con dominio real, mejor `spa_prerender`.

- Logo oficial del COB (PNG de Rosario, 04/11) en cabecera, hero y pie (`public/img/logo-cob.webp`, variante del pie `logo-cob-pie.webp` con el texto en claro y el laberinto cyan intacto); favicon propio del laberinto (solo `public/favicon.ico` 16/32/48/256, como socio y CAI). Assets: `/workspace/cob/logo/gen_assets.py`.

## Pendientes (huecos con `data-pendiente`)
- Fotos: hero 4:3, #necesidad, #que-es, ejemplo de informe 16:9, fotos de los 2 autores (iniciales JF/JP).
- CTA de Ofelia `cob` (alta en el webchat pendiente; puede dar 404 hasta entonces).
- URLs: manual de aplicación, documentación (y tour/Supademo si se quiere).
- GA4 (`GA4_ID` placeholder en `src/main.js`; en *.sslip.io no se carga nunca; solo tras aceptar analítica).
- Contenido de las subpáginas. Dominio real (OK de Joaquín).

```
npm ci && npm run dev     # local
npm run build             # dist/
```
