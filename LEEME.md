# Cuadraditos Kiosco

Registro de ventas del kiosco: productos con ícono o foto, stock, ticket imprimible y caja del día.
Es la misma app para todos los clientes. Cada uno pone el nombre de su negocio tocando el título
(en modo edición) y elige en **Ajustes** si usa mesas (0 = solo mostrador) y si pide clave de administrador.
Los datos se guardan en cada dispositivo. Usá el botón de exportar para hacer copias de seguridad.

## Instalar
- **Android (Chrome):** abrí el link → menú ⋮ → *Instalar app*.
- **iPhone (Safari):** abrí el link → Compartir → *Agregar a inicio*.
- Abrila desde el ícono (no desde el navegador). La app muestra un número de equipo de 4 cifras;
  el código de activación (3 números) se saca con el generador de códigos.
- La primera vez necesita internet. Abrila dos veces con conexión para que quede todo guardado.

## Clientes de antes
- Los equipos activados con KyriKiosco o KariKiosco siguen activados (los códigos viejos sirven).
- Si en el celular se usaba KariKiosco, la primera vez que abre esta app se traen sus productos,
  ventas y activación, y queda configurada sin claves como estaba.

## Al actualizar
Cada vez que reemplaces `index.html`, subí la versión en `sw.js`:
`const VERSION = "kyrikiosco-v4";` → v5, v6…
