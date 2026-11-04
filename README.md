# vito-kuz.github.io

Vitaliy Kuzmych's portfolio website, published at **https://vito-kuz.github.io**.

## Assumptions (decisions made while building)

- **Update, 2026-11-04:** added your headshot, "Vancouver, WA" (site Contact section, `resume-public.md` and `resume.pdf`), and a one-line description on every coursework card. The descriptions summarize each school's official catalog (sources below). They describe what each course covers, not anything about your own work in it. The empty engineering-project card was removed; add one once you've done a project, so nothing on the site is made up.
- **Name on the site:** "Vitaliy Kuzmych", exactly as written in `resume-public.md`.
- **Sources used:** `resume-public.md` for everything about you; the Clark College and PSU catalogs for the course descriptions only.
- **Intro (two sentences):** written by rewording the resume's Objective and job list. Nothing new was added.
- **Project cards:** the resume has one personal project (salvage-vehicle restoration), so the cards also show three things from your church leadership bullets (equipment sign-out system, sheet-music archive, meeting-notes document).
- **Coursework cards:** one card per course named in the resume, each with a one-line summary of the official catalog description. MTH 261 is Introduction to Linear Algebra and USP 300U is Introduction to Urban Studies (PSU Bulletin).
- **Experience order:** newest first. Your church role is listed first because it is ongoing (Nov 2019 – present).
- **Contact:** your city (Vancouver, WA) and email (vitkuz3@gmail.com). No phone number or street address anywhere on the site or in the PDF.
- **Accent color:** one blue. Light mode is the default; dark mode turns on automatically if the visitor's phone or computer is set to dark mode, and there is also a "Dark mode / Light mode" button at the top.
- **Photo:** your headshot, shrunk to `images/photo.jpg` (about 30 KB) so it loads fast on phones. The grey placeholder `images/photo.svg` is kept in case you ever want it back.
- **resume.pdf:** made from `resume-public.md`, one page, US Letter size. If you change `resume-public.md`, the PDF does **not** update by itself; ask Claude to "regenerate resume.pdf from resume-public.md".

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The whole website (all the text lives here) |
| `styles.css` | Colors, fonts and layout |
| `resume.pdf` | The downloadable resume |
| `resume-public.md` | The resume text the site and PDF were built from |
| `images/photo.jpg` | Your photo, as shown on the site |
| `images/photo.svg` | The grey placeholder (not used now) |

## How to change text (on GitHub's website, no software needed)

1. Go to https://github.com/vito-kuz/vito-kuz.github.io and sign in.
2. Click **`index.html`**.
3. Click the **pencil icon** (✏️ "Edit this file") near the top right of the file.
4. Find the text you want to change. Tip: press **Ctrl+F** (Windows) or **Cmd+F** (Mac) and type a few words.
5. Change **only the words between the tags**. Example: in
   `<p>Systems of linear equations, …</p>`
   change the words and leave `<p>` and `</p>` alone.
6. Click the green **Commit changes…** button, then **Commit changes** again in the box that appears.

On a phone: the GitHub app can't edit files, but the GitHub website in Safari can. Open the file and tap the pencil the same way.

## How to swap in a different photo

1. Pick a photo, ideally square (same width and height), about 600 × 600 pixels. Rename it on your computer to **`photo.jpg`**.
2. On GitHub, open the **`images`** folder.
3. Click **Add file → Upload files**, drag in `photo.jpg`, and click **Commit changes**. It replaces the old one; nothing else needs editing.

The photo is shown as a circle, so keep your face near the center. Big phone photos (several MB) make the page slow on phones, so shrink it first if you can (on iPhone: share the photo to yourself by email and pick "Small" or "Medium").

## How long changes take to go live

- After you commit, GitHub rebuilds the site automatically. GitHub says it "can take up to 10 minutes" for changes to publish, and it is often sooner. (Source: [GitHub Docs, Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), checked 2026-11-03.)
- To watch it: open the **Actions** tab of the repository. A yellow dot means "publishing", a green check means "live", a red X means something went wrong.
- If you still see the old version, your browser may be showing a saved copy. Refresh the page (on iPhone, pull down to refresh) or open it in a private tab.

## For whoever maintains this later

Plain HTML and CSS, no frameworks and no build step. GitHub Pages serves `index.html` from the top folder of the default branch. The only JavaScript is a few lines for the light/dark button; the site works without it.

## Sources for the course descriptions (checked 2026-11-04)

- Clark College Catalog 2026-2027: [Engineering](https://catalog.clark.edu/course-descriptions/engr/) (Statics, Dynamics, Mechanics of Materials, Field Survey I, Basic AutoCAD, Basic SolidWorks, Engineering Sketching and Visualization), [Physics](https://catalog.clark.edu/course-descriptions/phys/), [Mathematics](https://catalog.clark.edu/course-descriptions/math/), [Chemistry](https://catalog.clark.edu/course-descriptions/chem/), [English](https://catalog.clark.edu/course-descriptions/engl/) (Technical Writing), [Communication Studies](https://catalog.clark.edu/course-descriptions/cmst/) (Public Speaking)
- PSU Bulletin 2026-2027: [MTH 261](https://pdx.smartcatalogiq.com/en/2026-2027/bulletin/courses/mth-mathematical-sciences/200/mth-261), [USP 300U](https://pdx.smartcatalogiq.com/en/2026-2027/bulletin/courses/usp-urban-studies-planning/300/usp-300u)

