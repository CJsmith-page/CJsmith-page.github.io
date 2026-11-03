# Cudjoe John Smith: Business Analyst Portfolio

A plain HTML and CSS website, hosted free on GitHub Pages. There's no build step, no frameworks and nothing to install.

## How the files are organised

```
portfolio/
├── index.html                               ← Homepage
├── 404.html                                 ← Shown for any broken link
├── assets/
│   └── css/style.css                        ← ONE file controls the look of every page
├── experience/                              ← "How I delivered it" pages
│   ├── 01-collateral-investigation/index.html
│   ├── 02-sla-performance/index.html
│   ├── 03-screening-delivery/index.html
│   └── 04-requirements-delivery/index.html
└── analysis/                                ← Power BI projects
    ├── 01-consumer-complaints/               page and images (project files live in the project repository)
    ├── 02-bank-consolidation/
    ├── 03-financial-crime/
    ├── 04-hotel-cancellations/
    └── 05-online-retail/
```

The numbers at the front of folder names keep them in display order. Pages link to each other in the same order using the Previous / Next buttons at the bottom of each page.

Each page lives in its own folder as `index.html`, so its web address stays clean, for example:
`https://cjsmith-page.github.io/analysis/01-consumer-complaints/`

## Contact details

Name, LinkedIn, GitHub and email are already filled in on every page. To change one, search all files for the old value and replace it (on GitHub, press `.` on the repository page to open the browser editor, which can search and replace across every file).

## Common edits

| I want to… | Edit this |
|---|---|
| Change text on any page | That page's `index.html`. Text sits between tags, e.g. `<p>Your text</p>` |
| Change colours or fonts everywhere | The `:root` block at the top of `assets/css/style.css` |
| Change the picture at the top of an experience page | The block marked `<!-- ===== HERO VISUAL (first screen) ===== -->`. Keep it simple enough to understand in 5 seconds |
| Add a step to "How I delivered it" | Copy one `<li class="step">…</li>` block and paste it below. Numbers update automatically |
| Edit a swimlane diagram | Change the text inside each `sl-box`. To move a step, change its `grid-row` (lane) and `grid-column` (position). Notes are in the "Swimlanes" section of `style.css`. On phones, swimlanes turn into a vertical list automatically, so keep the boxes in step order |
| Change a Power BI project's three-point summary | The `<ul class="glance">` near the top of that project's `index.html` |
| Replace a dashboard image | Overwrite `dashboard.png` in the project folder with a new image of the same name |
| Add a new experience page | Copy a folder in `experience/`, rename it with the next number (e.g. `05-new-project`), edit the text, add a card for it on the homepage, and update the Previous / Next links |
| Add a new Power BI project | Create a new GitHub repository for the project (README, dashboard/, sql/, data/, docs/). Then copy a folder in `analysis/`, rename it with the next number, update the text, images and repository links, add a card on the homepage, and update the Previous / Next links |

Each page is split into numbered sections with comments like `<!-- ===== 4. HOW I DELIVERED IT ===== -->`, so you can find your place quickly.

## Rules to keep the site credible

- Your résumé is not on the site. Share it directly when someone gets in touch.

- Only put numbers under **"What happened"** if you can defend them in an interview.
- Keep employers anonymised ("a global investment bank"). Your private résumé can name them.
- Never describe how a control was bypassed, or name internal systems.
- Anything recreated or synthetic stays labelled as such.
- Keep some detail for the interview: lessons learned, the full SQL and the stories behind the numbers.

## Preview on your own computer

Double-click `index.html` to open it in your browser. Links between pages work this way.

## Publish on GitHub Pages

Your site address will be **https://cjsmith-page.github.io**. For that address, the repository must be named exactly **`CJsmith-page.github.io`** (capital letters don't matter).

1. Open your repository on GitHub, go to **Settings**, and under **Repository name** rename it to `CJsmith-page.github.io`. (A repository with any other name is published at a longer address, such as `cjsmith-page.github.io/repository-name/`.)
2. Upload everything **inside** the `portfolio` folder to the top level of the repository: **Add file → Upload files**, then drag the files and folders in. Upload one folder at a time if the browser struggles.
3. Go to **Settings → Pages**. Under "Build and deployment", choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute or two, the site is live at `https://cjsmith-page.github.io`.

**Updating later:** edit a file on GitHub and click **Commit changes**. The site refreshes within a couple of minutes.

**File size:** the website repository holds only pages, styles and images. Data, SQL, dashboards and briefs live in each project's own repository.

**If something looks broken:** links and the stylesheet use relative paths such as `../../assets/css/style.css`. If you move a page to a different folder depth, update those paths to match.
