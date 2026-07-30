# Your Portfolio — Step by Step

## What's in this folder
- `index.html` — page structure (hero, changelog/projects, about, skills, contact)
- `style.css` — all styling
- `script.js` — tiny scroll-reveal effect, no build tools needed

Open `index.html` in your browser right now to see it live before changing anything.

## Step 1 — Add your real content
1. `index.html` → change `<title>` and the hero text (name, tagline, sub-text).
2. Duplicate the `<article class="release">...</article>` block inside `#work`
   once per project. Each one needs: version tag, status (Live/Beta), year,
   title, one-line description, 2–3 stats, tags, and a case-study link.
3. Fill in `#about`, `#skills`, and the email/LinkedIn/GitHub links in `#contact`.
4. Replace the four `00` placeholders in the hero metrics bar with real numbers.
5. If you have a resume PDF, add it as `resume.pdf` in this folder — the hero
   button already links to `/resume.pdf`.

## Step 2 — Put it on GitHub
```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
(Create the empty repo on github.com first, then run the commands above.)

## Step 3 — Connect Netlify to the repo
1. Go to https://app.netlify.com → **Add new site → Import an existing project**.
2. Choose **GitHub**, authorize Netlify, and pick your repo.
3. Build settings for this plain HTML site:
   - Build command: *(leave blank)*
   - Publish directory: `.` (the repo root, since `index.html` is at the top level)
4. Click **Deploy site**. Netlify gives you a live URL like `your-name.netlify.app`
   within about a minute.

## Step 4 — Auto-deploy on every change
Once connected, every `git push` to `main` triggers a new Netlify deploy
automatically — no extra steps needed.

## Step 5 — Custom domain (optional)
In Netlify: **Site settings → Domain management → Add a custom domain**,
then point your domain's DNS to Netlify following their on-screen instructions.

## Step 6 — Keep iterating
- Add a new project any time by duplicating a `.release` block and pushing.
- If the site grows past a single page, consider re-building it in React/Vite
  later — the current structure will translate directly into components
  (Hero, ReleaseCard, About, Skills, Contact).
