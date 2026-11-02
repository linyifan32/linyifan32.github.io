# Academic homepage — multi-page starter

## Files

| Path | Purpose |
|---|---|
| `index.html` | Home / about page |
| `research.html` | Research interests |
| `publications.html` | Publications and preprints |
| `education.html` | Education |
| `teaching.html` | Teaching and service |
| `assets/css/style.css` | Layout, colors, spacing and mobile styles |
| `assets/images/` | Add your photo here |
| `assets/files/` | Add CV, papers and slides here |
| `.nojekyll` | Serve plain static files on GitHub Pages |
| `.gitignore` | Ignore local editor/system files |

## Preview locally

Extract this archive and double-click `index.html`. Links and styles work without a server. Edit with VS Code or any text editor; save and refresh your browser.

Optional local server from this folder (if Python is installed):

```bash
python -m http.server 8000
```

Visit http://localhost:8000 and press Ctrl+C in the terminal to stop.

## Customize

1. Review the starter bio. Replace every square-bracketed placeholder in the five HTML files.
2. Add a photo at `assets/images/photo.jpg`; follow the comment above the monogram to replace it with an image in each HTML file.
3. Add your CV at `assets/files/cv.pdf` and uncomment the CV link.
4. Replace the contact placeholder with, for example:

```html
<a href="mailto:YOUR_EMAIL">YOUR_EMAIL</a>
```

5. In `publications.html`, duplicate the `<article class="paper">...</article>` block for each publication. Add real links:

```html
<div class="paper-links">
  <a href="assets/files/paper.pdf">Paper</a>
  <a href="https://arxiv.org/abs/YOUR_ID">arXiv</a>
</div>
```

6. Remove unused pages AND their navigation links from all remaining HTML files. Update each footer date.
7. Change the color variables at the top of `assets/css/style.css` if desired.

Do not use invented paper details or publish placeholders. Escape literal ampersands in HTML as `&amp;`. Preserve the HTML tags around the text you edit.

## Shared layout and navigation

The sidebar and footer are repeated in each HTML file so that this site works without JavaScript, a server, or a build step. When changing your name, affiliation, email, photo or navigation, update all five pages. The stylesheet is shared, so a CSS change applies everywhere. Each page marks only its own navigation link with `aria-current="page"`.

Keep all five HTML files in the repository root. A link such as `publications.html` opens a separate page; a link starting with `#` jumps within the current page. Do not move pages into subfolders without adjusting their relative links.

To add a page, copy an existing HTML file, change its `<title>` and `<main>` content, add its link to every sidebar, and move `aria-current="page"` to the correct link on the new page.

## Updating from the earlier single-page template

Back up any personal edits first. This ZIP contains starter content, not changes made on your own computer. Copy the five HTML files and the new stylesheet into your repository, then reapply your personal content to its appropriate page. Keep your existing photos and PDFs. Do not replace or delete your repository's `.git` directory.

## Publish in a NEW GitHub repository

Create an empty public repository named `YOUR_USERNAME.github.io` on GitHub. Do not initialize that new repository with a README, license or gitignore because this folder supplies its own files.

Open a terminal in this extracted folder, replace YOUR_USERNAME below, then run:

```bash
git init
git add .
git commit -m "Create academic homepage"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

If Git asks for your name and email, configure your commit identity and retry the commit. Follow the Git authentication prompt when pushing.

In the repository, open **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, and save. After deployment, visit `https://YOUR_USERNAME.github.io/`.

The `index.html` file must be at the repository root, alongside `assets`, not inside an additional `academic-homepage-multipage` directory. Push the extracted files, not the ZIP archive.

## If you ALREADY have a repository

Clone your existing repository, then copy these template files into that checkout. Review existing files first. Do not run the new-repository commands above inside a repository that already has history, and do not force-push. An existing Jekyll theme may contain conflicting index files, custom-domain settings, or deployment workflows; review those separately before publishing this replacement.

## Subsequent edits

From your repository folder:

```bash
git pull
# Edit files and save.
git status
git add .
git commit -m "Update homepage"
git push
```

Check `git status` before staging to ensure only intended files are included. The repository and uploaded files will be public.

## Reuse as a GitHub template

If you want other people to copy this repository using GitHub's template feature, enable **Template repository** in its Settings after uploading. This is optional for your own homepage.
