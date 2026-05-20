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

## Custom domain (yariv.barsheshat.com)

1. Add a file named `CNAME` to the repo root containing the single line:
   ```
   yariv.barsheshat.com
   ```
2. At your DNS provider for `barsheshat.com`, add one record:
   - Type: `CNAME`
   - Name/host: `yariv`
   - Value/target: `yarv.github.io.` (the trailing dot only matters if your DNS UI is strict about FQDNs)
3. In the repo's **Settings → Pages**, set the Custom domain field to `yariv.barsheshat.com` and tick **Enforce HTTPS** once GitHub finishes provisioning the certificate (usually under a minute after the DNS resolves).
