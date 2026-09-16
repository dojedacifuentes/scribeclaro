# ScribeClaroPUCV · Paneles

Sitio estático con los paneles de trabajo de **ScribeClaroPUCV** (Pontificia Universidad Católica de Valparaíso).

| Ruta | Página | Contenido |
|---|---|---|
| `/` | Índice | Portada con acceso a ambos paneles |
| `/estrategia` | Panel estratégico | Diagnóstico, FODA, posicionamiento, calendario editorial, recursos, cursos, herramientas de IA, plan 90/180/365, métricas |
| `/rrss` | Kit de redes sociales | Montaje de cuentas, medidas y límites, activos gráficos, calendario de 30 días, 40 copys, 12 reels, captación y producción |

## Estructura

```
index.html        Portada
estrategia.html   Panel estratégico  → /estrategia
rrss.html         Kit de redes       → /rrss
vercel.json       Clean URLs, redirecciones y cabeceras
```

No hay build ni dependencias: son tres páginas HTML autónomas (CSS y JS en línea, sin recursos externos).

## Desarrollo local

Abrir `index.html` en el navegador, o servir la carpeta:

```bash
npx serve .
```

## Despliegue en Vercel

Proyecto estático sin configuración adicional.

1. En Vercel: **Add New → Project → Import Git Repository** y elegir `dojedacifuentes/scribeclaro`.
2. Framework Preset: **Other**. Dejar vacíos Build Command y Output Directory (Root Directory: `./`).
3. **Deploy**.

Cada push a `main` genera un despliegue de producción; las ramas y pull requests generan despliegues de vista previa.

Alternativa por CLI:

```bash
npx vercel --prod
```

## Notas

- `cleanUrls` permite las rutas sin extensión `.html`.
- Se mantienen redirecciones desde los nombres antiguos `/panel-rrss` y `/panel-scribeclaro`.
