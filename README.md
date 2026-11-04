# vito-kuz.github.io

Vitaliy Kuzmych's portfolio website, published at **https://vito-kuz.github.io**.

## Assumptions (decisions made while building)

- **Name on the site:** "Vitaliy Kuzmych", exactly as written in `resume-public.md`.
- **Only source used:** `resume-public.md`. Every sentence on the site comes from it. Anything missing is marked **[ADD: …]** so you can see what still needs filling in.
- **Intro (two sentences):** written by rewording the resume's Objective and job list. Nothing new was added.
- **Project cards:** the resume has one personal project (salvage-vehicle restoration), so the cards also show three things from your church leadership bullets (equipment sign-out system, sheet-music archive, meeting-notes document), plus one empty **[ADD]** card for an engineering or class project.
- **Coursework cards:** one card per course named in the resume. The resume has no course descriptions, so each card says **[ADD: short description]**. For MTH 261 and USP 300U only the course codes are shown, because the resume doesn't give their titles.
- **Experience order:** newest first. Your church role is listed first because it is ongoing (Nov 2019 – present).
- **Contact:** email only (vitkuz3@gmail.com, from the resume). No phone number or address anywhere on the site or in the PDF.
- **Accent color:** one blue. Light mode is the default; dark mode turns on automatically if the visitor's phone or computer is set to dark mode, and there is also a "Dark mode / Light mode" button at the top.
- **Photo:** a grey placeholder picture until you add your own (see below).
- **resume.pdf:** made from `resume-public.md`, one page, US Letter size. If you change `resume-public.md`, the PDF does **not** update by itself; ask Claude to "regenerate resume.pdf from resume-public.md".

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The whole website (all the text lives here) |
| `styles.css` | Colors, fonts and layout |
| `resume.pdf` | The downloadable resume |
| `resume-public.md` | The resume text the site and PDF were built from |
| `images/photo.svg` | The placeholder photo |

## How to change text (on GitHub's website, no software needed)

1. Go to https://github.com/vito-kuz/vito-kuz.github.io and sign in.
2. Click **`index.html`**.
3. Click the **pencil icon** (✏️ "Edit this file") near the top right of the file.
4. Find the text you want to change. Tip: press **Ctrl+F** (Windows) or **Cmd+F** (Mac) and type a few words, or search for `[ADD` to find every placeholder.
5. Change **only the words between the tags**. Example: in
   `<p class="add">[ADD: short description]</p>`
   replace `[ADD: short description]` and leave `<p class="add">` and `</p>` alone.
   When you fill in a placeholder, you can also delete ` class="add"` so the text is no longer grey and italic.
6. Click the green **Commit changes…** button, then **Commit changes** again in the box that appears.

On a phone: the GitHub app can't edit files, but the GitHub website in Safari can. Open the file and tap the pencil the same way.

## How to swap in your photo

1. Pick a photo, ideally square (same width and height), at least 400 × 400 pixels. Rename it on your computer to **`photo.jpg`**.
2. On GitHub, open the **`images`** folder.
3. Click **Add file → Upload files**, drag in `photo.jpg`, and click **Commit changes**.
4. Go back, open **`index.html`**, click the pencil, and search (Ctrl+F / Cmd+F) for `images/photo.svg`.
5. Change `images/photo.svg` to `images/photo.jpg`. Leave everything else on that line as it is.
6. Click **Commit changes**.

The photo is shown as a circle, so keep your face near the center of the picture.

## How long changes take to go live

- After you commit, GitHub rebuilds the site automatically. GitHub says it "can take up to 10 minutes" for changes to publish, and it is often sooner. (Source: [GitHub Docs, Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), checked 2026-11-03.)
- To watch it: open the **Actions** tab of the repository. A yellow dot means "publishing", a green check means "live", a red X means something went wrong.
- If you still see the old version, your browser may be showing a saved copy. Refresh the page (on iPhone, pull down to refresh) or open it in a private tab.

## For whoever maintains this later

Plain HTML and CSS, no frameworks and no build step. GitHub Pages serves `index.html` from the top folder of the default branch. The only JavaScript is a few lines for the light/dark button; the site works without it.
