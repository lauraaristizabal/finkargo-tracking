# Finkargo · Tracking — Informe Ejecutivo "Underway"

Repositorio privado para **versionar mensualmente** el informe ejecutivo de la vertical
**Agéntica** de Producto (Laura Aristizabal, Senior PM · Finkargo).

## Qué es

Un informe ejecutivo en HTML, estilo consultora premium, que resume:

1. **Punto de partida** — rol y mandato de la vertical Agéntica.
2. **Entendimiento del negocio** — tesis Finkargo OS, modelo de negocio, contexto Serie B.
3. **Retos y oportunidades** — palancas a resolver durante Q3.
4. **Plan de acción Q3** — priorización de iniciativas desde la vertical, con recomendaciones propias.

El informe es un **documento vivo** ("underway" = en curso): se regenera cada mes para reflejar
el avance real del roadmap Q3 y la evolución del entendimiento. El historial de git es la línea de
tiempo del progreso.

## Convención de nombres

```
informes/underway-dd-mm-aaaa.html
```

Un archivo nuevo por versión mensual + un commit descriptivo. Ejemplo:

- `informes/underway-05-07-2026.html` — línea base tras el Discovery (jun–jul 2026).
- `informes/underway-05-08-2026.html` — corte de agosto (Logistics Agent, avance demo Serie B).
- `informes/underway-05-09-2026.html` — cierre de Q3 (Cashflow Orchestrator).

## Cómo se usa

Cada archivo es **self-contained**: se abre directamente en el navegador (doble clic o `file://`),
sin dependencias locales. Para exportar a PDF, imprimir desde el navegador (tiene estilos `@media print`).

## Publicación (GitHub Pages)

El repo se publica como sitio estático (GitHub Pages requiere repo público en el plan free).
Para que no sea indexable por buscadores y solo accesible por quien tenga el link:

- `robots.txt` en la raíz bloquea todo crawling (`Disallow: /`).
- Cada informe HTML debe incluir en el `<head>`:
  ```html
  <meta name="robots" content="noindex, nofollow, noarchive, nosnippet">
  <meta name="googlebot" content="noindex, nofollow">
  ```
- No hay `index.html` que liste los informes — cada versión solo es accesible con su URL exacta.
- No enlazar el sitio desde ningún lugar público (LinkedIn, sitios indexados, etc.).

## Estructura

```
finkargo-tracking/
├── README.md
├── assets/        # recursos compartidos opcionales (logos, css)
└── informes/      # una versión mensual del informe por archivo
```

---

_Confidencial · Finkargo — uso interno (Producto / C-Level)._
