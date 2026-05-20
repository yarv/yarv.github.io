# yarv.github.io

Personal homepage. Static HTML/CSS, no build step.

## Files

- `index.html` — page markup
- `style.css` — styles
- `headshot.png` — profile photo

## Deploy to GitHub Pages

1. Create a new public GitHub repo named exactly **`yarv.github.io`** (the name must match your username for a user site).
2. From inside this `website/` directory:
   ```sh
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin git@github.com:yarv/yarv.github.io.git
   git push -u origin main
   ```
3. In the repo's **Settings → Pages**, set Source to "Deploy from a branch", Branch `main`, folder `/ (root)`. The site appears at `https://yarv.github.io` within a minute or two.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Custom domain (optional)

You already own `barsheshat.com`. To use it:

1. Add a file named `CNAME` to the repo root containing the single line `barsheshat.com`.
2. At your DNS registrar, point the apex to GitHub Pages by creating four `A` records to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, and a `CNAME` record from `www` to `yarv.github.io`.
3. In **Settings → Pages**, fill in the Custom domain field. GitHub will provision an HTTPS certificate automatically.
