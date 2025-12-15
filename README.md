# Sitio Matrimonio (estático)

Este repo contiene una página estática en `index.html` lista para publicar en GitHub Pages.

## Publicación en GitHub Pages
1. Crea un repo vacío en tu cuenta (p. ej. `matrimonio`).
2. En tu terminal, dentro de esta carpeta:

```zsh
git init
# (Opcional) Evitar exponer tu identidad en commits
# Usa tu correo "noreply" de GitHub o uno genérico
# Sustituye <usuario> por tu username
# Puedes ver tu correo noreply en https://github.com/settings/emails

git config user.name "website-bot"
git config user.email "<usuario>@users.noreply.github.com"

git add .
git commit -m "Publicación sitio"

git branch -M main
git remote add origin https://github.com/<usuario>/<repo>.git
git push -u origin main
```

3. En GitHub: Settings → Pages → Build and deployment → Source: "Deploy from a branch". Selecciona `main` y carpeta `/root`.
4. Abre la URL: `https://<usuario>.github.io/<repo>/`.

## QR del sitio (opcional)
- Una vez publicada la URL, puedes generar un QR rápido:

```zsh
# Requiere qrencode (Linux)
sudo apt-get install -y qrencode  # Ubuntu/Debian
qrencode -o assets/qr.png -s 8 "https://<usuario>.github.io/<repo>/"
```

- Alternativa online (sin instalar nada):
  `https://api.qrserver.com/v1/create-qr-code/?size=512x512&data=https://<usuario>.github.io/<repo>/`

## Notas
- `index.html` es la entrada del sitio. Los assets están en `assets/`.
- No se guardan credenciales ni datos personales en el repo por defecto.
- Si deseas usar dominio propio, crea el archivo `CNAME` con tu dominio.
# Matrimonio-Maripi
