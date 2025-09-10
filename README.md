# IMT-247 · Instrumentación Industrial — Plantillas y Estructura de Proyecto

Repositorio base para **prácticas, guías y documentación** de la asignatura IMT-247 (UCB · Tarija).
Incluye:
- Configuración inicial (`README.md`, `.gitignore`, licencias).
- **Plantillas LaTeX** para reportes de prácticas (artículo) y presentaciones (Beamer).
- **Carpeta de ejemplo** con una estructura documental para proyectos P&ID y fichas técnicas.
- Contenedor `guias/` para alojar guías de trabajo (se añadirán en otra conversación).
- **CI opcional** para compilar LaTeX con GitHub Actions.

> Sugerencia: Código (scripts) bajo **MIT** y contenido educativo (plantillas/guías) bajo **CC BY 4.0**.

---

## Estructura

```
.
├── .github/
│   └── workflows/
│       └── latex.yml
├── plantillas/
│   └── latex/
│       ├── practica_imt247.tex
│       └── beamer_imt247.tex
├── proyecto-ejemplo/
│   ├── 00_Documentacion/
│   │   ├── 01_PID/
│   │   │   └── README.md
│   │   ├── 02_HojasTecnicas/
│   │   │   └── README.md
│   │   ├── 03_Cotizaciones/
│   │   │   └── README.md
│   │   └── 04_Listados/
│   │       └── README.md
│   └── README.md
├── guias/
│   └── README.md
├── .gitignore
├── LICENSE        (MIT — para código)
├── LICENSE-docs   (CC BY 4.0 — para materiales docentes)
└── README.md
```

## Uso rápido

1) **Coloca** tus plantillas y estructura reales en las carpetas correspondientes.
2) Compila LaTeX localmente (ejemplo con `latexmk`):
   ```bash
   latexmk -pdf -interaction=nonstopmode plantillas/latex/practica_imt247.tex
   latexmk -pdf -interaction=nonstopmode plantillas/latex/beamer_imt247.tex
   ```
3) (Opcional) **CI**: en GitHub, activa *Actions*. El flujo `latex.yml` compila automáticamente los `.tex` dentro de `plantillas/latex/` tras cada push.

## Publicación

- Crea el repo en GitHub (vacío) y luego:
  ```bash
  git init
  git add .
  git commit -m "Estructura base IMT-247"
  git branch -M main
  git remote add origin git@github.com:USUARIO/NOMBRE_REPO.git
  git push -u origin main
  ```

> Ajusta el *remote* SSH a tu cuenta y nombre de repositorio.

---

## Buenas prácticas
- Mantén **nombres consistentes** para instrumentos y lazos (según ISA/ISO).
- Versiona **diagramas P&ID** (formato editable preferido) y exporta **PDFs** para revisión.
- Agrega `docs/` o `pages/` si quieres publicar guías con GitHub Pages.
- Usa *issues* y *milestones* para seguimiento de prácticas/proyectos.

---

© 2025-09-10 — UCB · IMT-247 Tarija. Ver licencias incluidas.
