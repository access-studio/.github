# Access Studio

Web accessibility audits for small and medium businesses. **Español más abajo.**

## AccessStudioBot

If you saw `AccessStudioBot` in your logs, it was us. Our crawler identifies itself with Chromium's user agent followed by:

```
AccessStudioBot/1.0 (+https://github.com/access-studio)
```

### What it does

- It lists the pages of a website and checks their accessibility (WCAG 2.2), for audits the site's owner has asked for.
- It may also make an **inventory only** of a public site, to study our costs and test our crawler: it records the structure of the pages (paths and hashes), not their text, images or screenshots.

### How it behaves

- It reads and respects `robots.txt` before anything else.
- At most **30 pages a minute** and **2 at a time**, and slower if your site answers slowly or with `429` or `503`. It honours `Retry-After`.
- It **stops** when it meets bot protection (a challenge, a captcha, a block). It never tries to get round it.
- It **never sends forms, buys, or creates accounts**. Requests other than `GET` and `HEAD` are refused inside the browser.

### How to block it or limit it

Add this to your `robots.txt`:

```
User-agent: AccessStudioBot
Disallow: /
```

A group for `AccessStudioBot` **replaces** your `*` group for us (RFC 9309). To keep us out of some paths only, repeat in our group every rule of your `*` group you want us to follow.

### What we keep

- From an inventory only: the structure (paths, page counts, hashes). No text, images or screenshots.
- From an audit the owner asked for: captures of the pages, deleted 90 days after the audit closes.
- From an internal test of our own system: anonymised figures only; everything else is deleted.

### Contact

Open an issue in [access-studio/.github](https://github.com/access-studio/.github/issues) to ask us anything, to report a problem, or to ask us to delete what we keep about your site. Please do not post personal data there: say you want to be contacted and we will reply.

---

# Access Studio (español)

Auditorías de accesibilidad web para pequeñas y medianas empresas.

## AccessStudioBot

Si has visto `AccessStudioBot` en tus registros, éramos nosotros. Nuestro rastreador se identifica con el user agent de Chromium seguido de:

```
AccessStudioBot/1.0 (+https://github.com/access-studio)
```

### Qué hace

- Lista las páginas de un sitio web y revisa su accesibilidad (WCAG 2.2), en auditorías que ha pedido el dueño del sitio.
- También puede hacer **solo un inventario** de un sitio público, para estudiar nuestros costes y probar el rastreador: guarda la estructura de las páginas (rutas y hashes), no sus textos, imágenes ni capturas.

### Cómo se comporta

- Lee y respeta `robots.txt` antes que nada.
- Como máximo **30 páginas por minuto** y **2 a la vez**, y más despacio si tu web responde lenta o con `429` o `503`. Respeta `Retry-After`.
- Se **detiene** ante cualquier protección antibots (un reto, un captcha, un bloqueo). Nunca intenta saltarla.
- **Nunca envía formularios, compra ni crea cuentas.** Las peticiones distintas de `GET` y `HEAD` se rechazan dentro del navegador.

### Cómo bloquearlo o limitarlo

Añade esto a tu `robots.txt`:

```
User-agent: AccessStudioBot
Disallow: /
```

Un grupo para `AccessStudioBot` **sustituye** a tu grupo `*` para nosotros (RFC 9309). Si solo quieres dejarnos fuera de algunas rutas, repite en nuestro grupo las reglas de `*` que quieras que sigamos.

### Qué guardamos

- De un inventario: la estructura (rutas, número de páginas, hashes). Ni textos, ni imágenes, ni capturas.
- De una auditoría encargada por el dueño: capturas de las páginas, que se borran 90 días después de cerrar la auditoría.
- De una prueba interna de nuestro sistema: solo cifras anonimizadas; todo lo demás se borra.

### Contacto

Abre una incidencia en [access-studio/.github](https://github.com/access-studio/.github/issues) para preguntarnos, avisarnos de un problema o pedirnos que borremos lo que tengamos de tu sitio. No pongas datos personales ahí: di que quieres que te contactemos y te responderemos.
