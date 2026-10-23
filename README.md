# Tony Bruce: Portfolio

A personal portfolio built with plain HTML5, CSS3 and vanilla JavaScript. No build step, no dependencies.

## Project structure

```
index.html      Page markup (all sections)
style.css       Styles, theme tokens, responsive rules
script.js       Theme toggle, mobile menu, active nav link, scroll reveal
assets/
  profile.jpg   Your portrait (you supply this)
  resume.pdf    Your résumé (you supply this)
  README.md     Notes on the two files above
```

## Before you publish: add your two files

1. Copy your photograph to `assets/profile.jpg`. A portrait-orientation photo (about 4:5, for example 800 x 1000 px) works best. It is cropped with `object-fit: cover`; if your face sits too high or low, change `object-position` in the `.portrait-frame img` rule in `style.css`.
2. Copy your résumé PDF to `assets/resume.pdf`.

Until those files exist, the hero shows a "TB" placeholder and the résumé links will not open a file.

## Things to confirm or add

- **SGPA:** your résumé lists 9.7, but it is intentionally not shown. If it is current, uncomment the SGPA row in the About section of `index.html`.
- **LinkedIn:** no URL was supplied, so none is shown. Add your real profile link where the comment in the Contact section indicates (and in the footer if you like).
- **Certifications:** the Experience section says "None listed yet". Replace that line with real entries when you have them.
- **Live demos:** none of the four projects has a hosted demo, so each card has a case study instead. If you deploy one, add a "Live demo" link next to "Source code" in that card.
- **Project case studies:** these are written from your project descriptions. Check each against its repository and edit anything that is not accurate.

## Test locally

Open `index.html` directly in a browser, or serve the folder:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000. Check the following:

- Theme toggle switches and the choice survives a reload.
- At widths below 900 px the menu button opens and closes the navigation (also with Escape).
- Every navigation link scrolls to its section.
- Tab through the page: every control shows a visible focus ring.
- No horizontal scrolling at 360 px width.

## Deploy to GitHub Pages

1. Create a repository on GitHub (for example `portfolio`) and push these files so that `index.html` is at the repository root.

   ```
   git init
   git add .
   git commit -m "Add portfolio site"
   git branch -M main
   git remote add origin https://github.com/TonyBruce07/portfolio.git
   git push -u origin main
   ```

2. On GitHub, open **Settings > Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the `main` branch and the `/ (root)` folder, then save.
4. After a minute or two the site is live at `https://tonybruce07.github.io/portfolio/`.

All local paths in the site are relative (`style.css`, `assets/profile.jpg`), so it works under a project URL like the one above. Name the repository `TonyBruce07.github.io` instead if you want the site at `https://tonybruce07.github.io/`.
