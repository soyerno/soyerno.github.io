# soyerno.github.io

Sitio de [GitHub Pages](https://pages.github.com/) servido en **https://soyerno.github.io**.

Es una landing mínima que **apunta** a mi perfil de GitHub — la única fuente de verdad
de mi bio, stack, proyectos y contacto:

➡️ **https://github.com/soyerno**

## ¿Por qué un redirect?

Antes tenía el mismo contenido duplicado en tres lugares (este landing, el perfil de
GitHub y el portfolio). Mantener tres copias en sync no escala. Dejé **una sola**: el
[profile README](https://github.com/soyerno) (repo [`soyerno/soyerno`](https://github.com/soyerno/soyerno)),
que es el más rico. Esta URL quedó como puntero hacia él.

## Cómo funciona

[`index.html`](index.html) es una tarjeta estática con un botón **Ver mi perfil de GitHub →**.
Sin auto-redirect: el visitante decide cuándo ir al perfil.

`<link rel="canonical">` apunta al perfil para señalar a los buscadores cuál es el destino canónico.

## Desarrollo

Es un único archivo estático, sin build ni dependencias.

```sh
# Preview local
python3 -m http.server 8000   # http://localhost:8000
```

## Deploy

GitHub Pages publica automáticamente desde la rama `main`. Mergear acá = sitio live.
