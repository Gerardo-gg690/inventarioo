# Bon House - Inventario

Sistema de inventario con presentaciones (fardo, paquete, unidad), conteos por fecha,
movimientos, compras/facturas y PDF por proveedor. Es una página estática: no necesita servidor.

## Subirlo a GitHub (con GitHub Pages)
1. Crea un repositorio nuevo en github.com (por ejemplo `bonhouse-inventario`).
2. Sube estos archivos a la raíz: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`.
3. En el repositorio: Settings > Pages > Source: "Deploy from a branch" > Branch `main` / carpeta `/ (root)` > Save.
4. En un par de minutos tendrás el enlace: `https://TU-USUARIO.github.io/bonhouse-inventario/`.

## Usarlo en el celular
Abre el enlace en Chrome > menú (tres puntos) > "Instalar app" o "Agregar a pantalla de inicio".

## Convertirlo en APK
Con el enlace de GitHub Pages ya publicado, entra a pwabuilder.com, pega el enlace y descarga el paquete de Android.

## Importante
- Los datos se guardan en el navegador de cada dispositivo (no se comparten entre celulares).
  Usa "Movimientos y respaldo" > "Descargar respaldo" para guardar copias y pasarlas a otro equipo.
- La sincronización en la nube solo existe dentro de Claude; en GitHub funciona sin ella.
- Los PDF necesitan internet la primera vez (cargan la librería jsPDF desde cdnjs).
