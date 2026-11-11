# Project page: What Should World Models Forget?

Static site (a single HTML file, no build step) for the NeurIPS 2026 Workshop on Continual World Models paper.

```
index.html            the whole page (styles and script are inside it; same design as the AuditEar page)
assets/paper.pdf      final camera-ready PDF
assets/logos/umd.png  UMD logo
assets/fig1_a.png     Figure 1(a), used as the link-preview image
assets/fig1_b.png     Figure 1(b)
```

## Deploy on GitHub Pages

The poster QR code and the page's link previews assume this URL:
**https://nishitanand.github.io/what-should-world-models-forget/**

1. On GitHub, create a public repository named `what-should-world-models-forget`.
2. Push the contents of this folder (not the folder itself) to the `main` branch:
   ```
   cd website
   git init
   git add .
   git commit -m "Project page"
   git branch -M main
   git remote add origin https://github.com/nishitanand/what-should-world-models-forget.git
   git push -u origin main
   ```
3. In the repository, open Settings → Pages, set Source to "Deploy from a branch", choose `main` and `/ (root)`, and save.
4. After a minute or two, the site is live at the URL above.

If you use a different repository name, the URL changes. In that case, update the `og:url` and `og:image` lines in `index.html` and regenerate the poster QR code.

## Preview locally

```
cd website
python3 -m http.server 8000
```
Then open http://localhost:8000.
