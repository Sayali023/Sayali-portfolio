# Sayali Pawar — Developer Portfolio

This is the exact portfolio page from the Claude Artifact, exported unchanged as `index.html`.
It is plain HTML, CSS and JavaScript with **no build step**, so it deploys to Vercel as a static site.
It was not rewritten into React/Vite, because that would change the original implementation.

## Files
- `index.html` — the whole site (styles, scripts, logos and certificate images are inside it)
- `assets/Sayali_Pawar_Resume.pdf` — **you must add this** (your real resume). The `assets/` folder is already here.
- `package.json` — only provides `npm start` for local preview

## Add your resume
Copy your PDF into the `assets/` folder and name it exactly `Sayali_Pawar_Resume.pdf`.
Until it exists, the Download Resume buttons show a "Resume not found" message.

## Contact details
Email, GitHub and LinkedIn are set in the `PROFILE` block in `index.html` (search for `const PROFILE=`). The contact form opens your email app (mailto); it has no backend and does not store or send messages itself.

## Run locally
```bash
npm start            # opens http://localhost:3000  (needs Node.js)
# or without Node:
python3 -m http.server 3000
```

## Deploy: GitHub, then Vercel
```bash
git init
git add .
git commit -m "Add portfolio"
git branch -M main
git remote add origin https://github.com/Sayali023/portfolio.git   # create this empty repo on github.com first
git push -u origin main
```
Then on vercel.com: **Add New → Project → import the repo**. Set Framework Preset to **Other**,
leave Build Command and Output Directory empty, and press Deploy.
Every later `git push` redeploys automatically.

## Known limits
- Google Fonts (Cormorant Garamond, Inter) load from Google; offline they fall back to Georgia and system fonts.
- Certificate images are compressed copies embedded in `index.html`. Keep your originals separately.
- Project cards have no GitHub or Live Demo buttons because no URLs are configured yet.
- The Coursera verify link uses the ID printed on the certificate; test it after deploying.
