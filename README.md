# Bon House · Inventario con Firebase

Se mantiene el diseño y la lógica del inventario original. La nueva versión incorpora inicio de sesión con Firebase Authentication y sincronización del documento `inv/main` en Firestore.

## Configuración
1. Crea un proyecto **nuevo** en Firebase (no reutilices TimeCore). Agrega una app Web y copia los valores al archivo `firebase-config.js`.
2. Activa Authentication > Método de acceso > Correo electrónico/contraseña. Crea manualmente las cuentas autorizadas en Authentication > Usuarios.
3. Copia los UID de esas cuentas y reemplaza `REEMPLAZAR_UID_ADMIN` en `firestore.rules`. Puedes añadir más UID separados por comas.
4. Crea la base de datos Firestore. Copia las reglas desde `firestore.rules` y publícalas. **Nunca** uses reglas abiertas.
5. Sube a GitHub Pages todos los archivos de esta carpeta, incluyendo `firebase-config.js`.
6. Inicia sesión. Antes de importar, entra a la versión anterior en el dispositivo que tenga tus datos, ve a **Movimientos y respaldo > Descargar respaldo**. En la versión nueva, en ese mismo dispositivo y navegador, pulsa **Subir datos de este dispositivo** para migrarlos. Verifica que aparezcan en un segundo dispositivo.

## Advertencias importantes
- El botón **Subir datos de este dispositivo** reemplaza la copia en Firebase: úsalo solo para migración o recuperación intencional.
- El inventario usa un documento compartido: si dos personas editan simultáneamente, la última escritura puede sobrescribir cambios. No es todavía una solución transaccional multiusuario para uso intensivo.
- Firestore tiene un límite de 1 MiB por documento. Si los historiales o facturas crecen, habrá que separar registros en colecciones.
- No se sincronizan imágenes binarias de facturas; el ZIP original contiene referencias/datos del sistema según su implementación.
- Antes de desplegar, prueba con un respaldo. No elimines datos originales.
