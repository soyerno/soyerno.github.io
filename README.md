# soyerno.github.io

Sitio de [GitHub Pages](https://pages.github.com/) servido en **https://soyerno.github.io**.

Es solo un **redirect** a mi perfil de GitHub — la única fuente de verdad de mi bio,
stack, proyectos y contacto:

➡️ **https://github.com/soyerno**

## ¿Por qué un redirect?

Antes tenía el mismo contenido duplicado en tres lugares (este landing, el perfil de
GitHub y el portfolio). Mantener tres copias en sync no escala. Dejé **una sola**: el
[profile README](https://github.com/soyerno) (repo [`soyerno/soyerno`](https://github.com/soyerno/soyerno)),
que es el más rico. Esta URL quedó como puntero hacia él.

## Cómo funciona

[`index.html`](index.html) redirige por tres vías, de la más rápida a la más resiliente:

1. `<meta http-equiv="refresh">` — redirect inmediato, funciona sin JS.
2. `location.replace()` — redirect por JS (no ensucia el historial del browser).
3. Un botón visible **Ir al perfil →** — fallback accesible si todo lo demás falla.

`<link rel="canonical">` apunta al perfil para que los buscadores indexen ese destino, no esta URL.

## Desarrollo

Es un único archivo estático, sin build ni dependencias.

```sh
# Preview local
python3 -m http.server 8000   # http://localhost:8000
```

## Deploy

GitHub Pages publica automáticamente desde la rama `main`. Mergear acá = sitio live.
