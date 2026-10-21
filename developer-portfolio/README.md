# Naol Takele — Developer Portfolio

A static, responsive portfolio built with HTML5, CSS3 and vanilla JavaScript (ES6+). No frameworks, no build step.

## 1. Overview
Sections: Home, About, Skills, Projects (with filters), Resume, Contact (with validated form). Dark theme by default, light theme available and remembered.

Featured projects:
- **NT Music Player** — music player project using HTML, CSS, JavaScript, Java, Spring Boot, and MongoDB.
- **BMI Calculator** — responsive BMI calculator built with HTML, CSS, and JavaScript.
- **Personal Portifolio** — responsive portfolio site built with HTML5, CSS3, and JavaScript ES6+.

## 2. Technologies
HTML5, CSS3 (custom properties, Flexbox, Grid), JavaScript ES6+, Intersection Observer, LocalStorage, inline SVG icons, Plus Jakarta Sans (Google Fonts, with system fallback).

## 3. Folder structure
```
developer-portfolio/
├── index.html
├── style.css
├── script.js
├── README.md
├── .gitignore
├── assets/
│   ├── images/   profile.jpg, project-1.svg, project-2.svg, project-3.svg
│   │             (legacy project JPGs are not used by the project cards)
│   └── icons/    favicon.svg
└── resume/       Naol-Takele-CV.pdf
```

## 4. Run locally
- Simplest: double-click `index.html`.
- Better: open the folder in VS Code, install **Live Server**, right-click `index.html` → *Open with Live Server*.

## 5. Customize
- **Text:** edit `index.html` (hero, about, skills, resume).
- **Colors:** edit the variables at the top of `style.css` (`:root` for dark, `:root[data-theme="light"]` for light).
- **Skills:** chips are `<li>` items in each skill card. Percentage bars use `--w` and `aria-valuenow` on each `.meter-track`; change both together.
- **Projects:** edit the `PROJECTS` array at the top of `script.js` (title, description, image, tags, categories, URLs).

## 6. Profile and project images
The project cards use three illustrated previews: `project-1.svg` (NT Music Player), `project-2.svg` (BMI Calculator), and `project-3.svg` (Personal Portifolio). To use screenshots instead, add them under `assets/images/` and update the image paths in the `PROJECTS` array in `script.js`.
- Profile: your portrait is already in place (`profile.jpg`, 800×800). To change it, overwrite that file with a square image.
- Project screenshots: use a 16:10 aspect ratio, about 800×500. Keep each file small (under ~200 KB) for fast loading.

## 7. Resume PDF
`resume/Naol-Takele-CV.pdf` is a one-page CV built from the details you provided. To update it, export a new PDF and overwrite that file using the same name. Both resume buttons use that path.

## 8. Contact links
In `script.js`, edit `CONFIG`: `email`, `phone`, `github`, `linkedin` (a username or a full URL). GitHub and LinkedIn are still placeholders and stay non-clickable until you set them.

## 9. Contact form delivery
A static site cannot send email by itself. Until you configure a service, the form validates input and tells the visitor the message was **not** sent.

**Formspree (easy):**
1. Create a free form at formspree.io and copy its endpoint (looks like `https://formspree.io/f/xxxxxxx`).
2. Paste it into `CONFIG.formEndpoint` in `script.js`.

**Other options:** Netlify Forms, Web3Forms, or your own backend API that accepts JSON `{name, email, subject, message}` and returns a 2xx status. Success is only shown when the response is OK.

## 10. Deploy to GitHub Pages
1. Create a GitHub repository and push this folder's contents (`index.html` at the repo root).
2. Repo → **Settings → Pages**.
3. Under *Build and deployment*, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. After a minute your site appears at `https://naol-ambisa.github.io/REPO_NAME/` (replace `REPO_NAME` with your repository name).

## 11. Deploy to Netlify
1. Sign in at netlify.com → **Add new site → Deploy manually**, and drag the project folder in; or
2. **Import from Git**, pick your repo, leave *build command* empty and set *publish directory* to `.`.

## 12. Deploy to Vercel
1. Sign in at vercel.com → **Add New → Project** and import your GitHub repo.
2. Framework preset: **Other**. Leave build command and output directory empty.
3. Click **Deploy**.

## Pre-launch checklist
- [ ] Replace the three illustrated project previews with screenshots
- [ ] Confirm the email address (`naolambisa21@gmail.com`)
- [ ] Set email, GitHub and LinkedIn in `CONFIG`
- [ ] Add real project URLs (buttons stay disabled until you do)
- [ ] Configure the form endpoint
- [ ] Update `og:image` / add an `og:url` once deployed
