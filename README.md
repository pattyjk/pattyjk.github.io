# Patrick Kearns — Research Site

A Jekyll site for GitHub Pages, built around Patrick Kearns' CV and Google Scholar record.

## What's in here

```
_config.yml           site settings — nav, email, Scholar link
_data/publications.yml  all 40 publications, generated from your Scholar CSV export
index.md               About / home page
research.md            Research themes
publications.md        Full publication list, grouped by year (reads from _data)
teaching.md            Courses & workshops
contact.md             Contact info
_layouts/default.html  page shell
_includes/nav.html      top navigation
_includes/footer.html   footer
_includes/branch-motif.svg   the branching-line hero graphic
assets/css/style.css   all styling
assets/images/headshot.jpg
```

## 1. Before you publish — two things to change

Open `_config.yml` and update:

```yaml
url: "https://YOUR-GITHUB-USERNAME.github.io"
baseurl: "/YOUR-REPO-NAME"
```

- If your repo will be named `YOUR-GITHUB-USERNAME.github.io` (a "user site"), leave `baseurl` as an empty string `""` instead.
- Otherwise, if you create a repo called e.g. `kearns-lab`, set `baseurl: "/kearns-lab"`.

## 2. Publish to GitHub Pages

```bash
# from inside this folder
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root)**.
Your site will be live in a minute or two at the URL you set above.

## 3. Preview locally (optional but recommended)

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Editing content later

- **Add a publication:** edit `_data/publications.yml` — add a new entry at the top with `authors`, `title`, `journal`, `volume`, `number`, `pages`, `year`. Wrap "Kearns" in `**double asterisks**` in the authors field to keep it bold.
- **Update your bio / research blurbs:** edit `index.md` and `research.md` directly — they're plain Markdown with a bit of HTML for layout.
- **Add or rename courses:** edit `teaching.md`.
- **Change colors/fonts:** all in `assets/css/style.css`, values are set as CSS variables at the top of the file.
- **Swap the headshot:** replace `assets/images/headshot.jpg` with a new image of the same filename (roughly square works best).

## Notes

- The publications list was generated from your Google Scholar CSV export (40 entries, 2012–2026) and sorted newest-first.
- The three "in review/revision" manuscripts and the abstracts/talks list from your CV weren't included in `publications.yml` — let me know if you'd like those added as a separate section.
- The hero graphic is a generated branching-line motif (nodding to both tidal-creek drainage patterns and phylogenetic trees) — it's pure SVG, no image file needed.
