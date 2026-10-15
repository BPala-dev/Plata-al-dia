# Plata al Día

App web para anotar ingresos y gastos y ver cómo viene el mes: balance, presupuestos por categoría, reportes y exportación a CSV.

- Funciona sin conexión y se puede instalar en el teléfono como una app (PWA).
- Los datos se guardan solo en el navegador de cada dispositivo (`localStorage`). No hay servidor ni cuentas.
- Para no perder datos, usá **Ajustes → Guardar copia de seguridad** de vez en cuando.

## Usarla

Publicada con GitHub Pages: https://bpala-dev.github.io/Plata-al-dia/

**Instalar en el celular**
- Android (Chrome): menú ⋮ → *Instalar app* / *Agregar a la pantalla principal*.
- iPhone (Safari): botón Compartir → *Agregar a inicio*.

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | Toda la app (HTML, CSS y JS en un solo archivo) |
| `manifest.webmanifest` | Nombre, colores e íconos para instalarla |
| `sw.js` | Service worker: cache para que abra sin conexión |
| `icons/` | Íconos de la app |

## Publicar cambios

1. Editá `index.html`.
2. En `sw.js`, subí `VERSION` (por ejemplo `"v1"` → `"v2"`) para que los teléfonos que ya la tienen instalada tomen la versión nueva.
3. Hacé commit y push a `main`. GitHub Pages la actualiza en uno o dos minutos.

## Probar en la PC

El service worker no funciona abriendo el archivo con doble clic; levantá un servidor local en esta carpeta:

```
npx serve .
```

o `python -m http.server 8000`, y abrí http://localhost:8000.
