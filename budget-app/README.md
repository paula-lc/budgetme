# Presupuesto al detalle

App para gestionar tu presupuesto mensual, estilo hoja de cálculo.

## Qué hace

- Pestañas de **Gastos fijos**, **Gastos variables** y **Ahorros** (y las que quieras crear), con edición directa de categorías, líneas e importes.
- Ingresos por mes, arrastre del sobrante al mes siguiente y previsión de cierre.
- Objetivos de ahorro, gasto e inversión, con reparto por prioridad.
- Vencimientos periódicos (trimestrales, anuales, préstamos por cuotas), control de efectivo, previsión por años e inversión.
- Importación de movimientos bancarios (CSV/pegado) con clasificación automática.
- Deshacer / rehacer (Ctrl+Z / Ctrl+Y).
- Perfiles locales: varias personas pueden usar la app en el mismo navegador sin mezclar datos.

Los datos se guardan **solo en el navegador** (`localStorage`). No hay servidor: los perfiles separan datos, pero no son un sistema de seguridad.

## Cómo usarla

Sirve la carpeta raíz del repositorio con cualquier servidor estático (o GitHub Pages) y abre `index.html`.

### Publicarla con GitHub Pages

1. Ve a **Settings → Pages** en este repositorio.
2. En "Source", selecciona la rama `main` y la carpeta `/ (root)`.
3. Guarda. En unos minutos la app estará disponible en
   `https://<tu-usuario>.github.io/<nombre-del-repo>/`.

## Estructura

```
/
├── index.html      # Plantilla y lógica de la app
├── support.js      # Runtime que renderiza la plantilla con React (generado, no editar)
├── vendor/         # React 18.3.1 (UMD), servido localmente en vez de desde un CDN
└── budget-app/README.md
```

## Tecnología

HTML, CSS y JavaScript sobre React 18 (incluido en `vendor/`). Sin paso de build.
