# QR reprogramables — cómo montarlo

20 códigos QR que imprimes **ahora** y programas **después**, igual que un chip NFC.
Cada sticker apunta a una dirección fija tuya; tú decides a dónde salta esa dirección,
y lo cambias las veces que quieras sin volver a imprimir.

Costo: **$0**. Sin mensualidad, sin dominio, sin caducidad.

---

## 1. Publicarlo (una sola vez, ~5 minutos)

1. Entra a **github.com** y crea una cuenta si no tienes.
2. Botón **New repository**. Ponle un nombre **corto** — `qr` es ideal, porque
   forma parte de la URL y entre más corta, menos denso sale el QR.
   Déjalo en **Public** (es requisito para el hosting gratis) y crea el repo.
3. **Add file → Upload files**. Arrastra ahí el *contenido* de esta carpeta:
   las 20 carpetas (`01` … `20`), el `index.html` y el archivo `.nojekyll`.
   Abajo, **Commit changes**.
4. **Settings → Pages**. En *Source* elige **Deploy from a branch**,
   rama `main`, carpeta `/ (root)`. **Save**.
5. Espera 1–2 minutos. Ya está en línea.

Te queda así (cambia `TUUSUARIO` por el tuyo):

| Qué | Dirección |
|---|---|
| Tu panel | `https://TUUSUARIO.github.io/qr/` |
| Código 01 | `https://TUUSUARIO.github.io/qr/01/` |
| Código 20 | `https://TUUSUARIO.github.io/qr/20/` |

---

## 2. Imprimir los stickers

Abre tu panel y pulsa **Imprimir hoja de stickers**. Salen los 20 QR en
cuadrícula, cada uno con su número visible y líneas punteadas para cortar.

El número impreso es lo que te dice cuál sticker es cuál cuando los repartas.
Apúntalo: *"el 07 se lo di a la panadería"*.

**Imprime solo después del paso 1**, cuando la dirección ya es definitiva.

---

## 3. Cambiar a dónde apunta un QR

En el panel, pulsa **Cambiar destino** en la fila del código. Se abre el editor
de GitHub en ese archivo. Cambia solo esta línea:

```js
var DESTINO = "";
```

por el enlace que quieras:

```js
var DESTINO = "https://wa.me/521555123456";
var NEGOCIO = "Panadería La Espiga";
```

Pulsa **Commit changes**. En ~30 segundos el QR impreso ya lleva al nuevo destino.

- `DESTINO` vacío = el sticker muestra *"Este código aún no está asignado"*.
  Es el estado de fábrica: el QR funciona, solo que todavía no lleva a ningún lado.
- `NEGOCIO` es solo para ti: aparece en tu panel para saber de quién es cada código.

Esto se hace igual desde el celular, con la app de GitHub o desde el navegador.

---

## Cosas que conviene saber

- **El repo es público.** Cualquiera que encuentre la dirección puede ver a dónde
  apuntan tus códigos. No son secretos, son enlaces de marketing — pero no pongas
  ahí nada privado.
- **Un QR por negocio.** Si el negocio 07 no acepta, reasignas solo el 07 y los
  otros 19 siguen intactos.
- **No hay contador de escaneos.** Si más adelante lo quieres, se puede añadir
  apuntando los destinos a enlaces con seguimiento.
- **¿Quieres tu propio dominio después?** *Settings → Pages → Custom domain*.
  Los QR ya impresos seguirían funcionando mientras conserves el repo.
- **Añadir más códigos:** duplica cualquier carpeta (`21`, `22`…) y cambia
  `TOTAL = 20` en `index.html`.
