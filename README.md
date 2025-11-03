
# Dashboard Sanaré & Nomad — Interactivo

## Contenido
- `index.html`: Dashboard con gráficos que se renderizan al abrir cada pestaña. Carga Plotly desde CDN.
- `recomendaciones_por_hoja.md`: Sugerencias específicas por hoja (calidad de datos, métricas y categorías).
- `exports/exports_Sanare` y `exports/exports_nomad`: CSVs de cada hoja para conexiones externas.

## Uso
1. Abre `index.html` en tu navegador o súbelo a GitHub Pages / Vercel.
2. Cambia de pestaña para que se dibujen los gráficos (render on‑demand).
3. Si algún gráfico no aparece, revisa:
   - Que la hoja tenga una **columna de fecha** válida.
   - Que exista una **métrica numérica** (por ejemplo `Total`, `Importe`, `Seguidores patrocinados`, `Visitas`).
   - Los valores con `$`, comas o texto pueden impedir el agregado. (Si lo necesitas, pídeme un limpiador de números.)

## Notas técnicas
- Plotly se carga desde CDN para asegurar compatibilidad.
- El script define `window.__figSpecs` antes de registrar cada figura y renderiza al activar la pestaña.
