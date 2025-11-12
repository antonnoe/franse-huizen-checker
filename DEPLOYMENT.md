# 🚀 Snelle Deployment Guide

## Stap 1: Upload naar GitHub

```bash
# In je lokale franse-huizen-checker folder:
git add .
git commit -m "Initial commit - Franse Huizen Tool"
git push origin main
```

## Stap 2: Activeer GitHub Pages

1. Ga naar: https://github.com/antonnoe/franse-huizen-checker/settings/pages
2. Bij **Source**: Selecteer **main** branch
3. Folder: **/ (root)**
4. Klik **Save**

## Stap 3: Wacht 2 minuten

Je site is live op: **https://antonnoe.github.io/franse-huizen-checker/**

## WordPress Integratie

### iFrame code voor in je artikel:

```html
<iframe 
  src="https://antonnoe.github.io/franse-huizen-checker/" 
  width="100%" 
  height="1200px"
  frameborder="0"
  style="border: none; display: block;">
</iframe>
```

### Waar te plakken:
1. WordPress → Artikel/Pagina bewerken
2. Voeg **Custom HTML** block toe (+ knop → Custom HTML)
3. Plak de iframe code
4. Publiceer!

## Klaar! 🎉

De tool draait nu op GitHub Pages en is te embedden in WordPress.

## Updates maken?

1. Bewerk `index.html`
2. `git add index.html`
3. `git commit -m "Update"`
4. `git push origin main`
5. Wacht 1-2 minuten → Live!

## Problemen?

- Check GitHub Actions tab voor deployment status
- Refresh hard (Ctrl+F5 of Cmd+Shift+R)
- Check Console (F12) voor errors
