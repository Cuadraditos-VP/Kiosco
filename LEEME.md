# Cuadraditos Kiosco

Registro de ventas del kiosco: productos con ícono o foto, stock, ticket imprimible y caja del día.
Es la misma app para todos los clientes. Cada uno pone el nombre de su negocio tocando el título
(en modo edición).

Por ahora es la **versión simple**: solo mostrador y sin clave de administrador.
Para habilitar mesas y clave (se eligen en Ajustes), cambiar en `index.html`:
`const VERSION_AVANZADA = false;` → `true`.
Los datos se guardan en cada dispositivo. Usá el botón de exportar para hacer copias de seguridad.

## Instalar
- **Android (Chrome):** abrí el link → menú ⋮ → *Instalar app*.
- **iPhone (Safari):** abrí el link → Compartir → *Agregar a inicio*.
- Abrila desde el ícono (no desde el navegador). La app muestra un número de equipo de 4 cifras;
  el código de activación (3 números) se saca con el generador de códigos.
- La primera vez necesita internet. Abrila dos veces con conexión para que quede todo guardado.

## Compartir el kiosco (dueño y encargado)
- El dueño entra a **Menú → Ajustes → Compartir el kiosco**. La app sube sus datos a internet y le da un
  código de 6 números. Con **Enviar invitación** manda el link y el código por WhatsApp.
- El encargado instala la app, la abre y en *¿Te invitaron a un kiosco?* escribe ese código. No necesita
  código de activación: solo puede usar el kiosco del dueño.
- El encargado puede vender y abrir y cerrar la caja. No puede cambiar productos, precios ni ajustes,
  ni ver el historial.
- **Cambiar código** saca a todos los que tenían el código anterior.
- El kiosco compartido necesita internet.

### Firebase
Usa el mismo proyecto que la lista del súper (`supermercado-ff56a`), en la sección `kioscos`.
En la consola de Firebase → Realtime Database → Reglas, agregar dentro de `"rules"`:

```json
"kioscos": {
  "$codigo": { ".read": true, ".write": true }
}
```

## Clientes de antes
- Los equipos activados con KyriKiosco o KariKiosco siguen activados (los códigos viejos sirven).
- Si en el celular se usaba KariKiosco, la primera vez que abre esta app se traen sus productos,
  ventas y activación.

## Al actualizar
Cada vez que reemplaces `index.html`, subí la versión en `sw.js`:
`const VERSION = "kyrikiosco-v8";` → v9, v10…
