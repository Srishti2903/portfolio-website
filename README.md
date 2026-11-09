
live at **[srishtigangolly.com](https://srishtigangolly.com)**.

It's a retro pixel desktop: the homepage contains icons you can open (and drag around), every page is a window, and there's a mailbox where visitors can write a letter or send a bouquet.

## Pages

| Page | File | What's on it |
| --- | --- | --- |
| Desktop (homepage) | `index.html` | Draggable icons, the menu bar, and the resizable `welcome.txt` window |
| About | `about.html` | Profile card, "for the resume" timeline and "beyond the resume" |
| Experience | `experience.html` | Roles as expandable dropdowns |
| Certifications | `certifications.html` | Certificate cards with credential links |
| Projects | `projects.html` | Links to the two case studies |
| DeerHacks | `deerhacks.html` | Case study with deerhacks ii / iii tabs |
| Ready, set, market | `rsm.html` | Case study with a clickable quiz phone |
| Writing | `writing.html` | Substack link and a writing-prompt generator |
| Mailbox | `mailbox.html` | Write a letter or build a bouquet |
| Old portfolio | `v1/` | The previous version of the site, kept as is |

`desktop.html` only forwards to the homepage, so older links keep working.

## Folders

```
portfolio/          the website, published as srishtigangolly.com
  img/site/         photos and artwork used by the pages
  img/doodle.png    the doodle logo, also the favicon
  js/srishti-os.js  the page runtime
  docs/             the RSM case-competition deck (PDF)
  v1/               the old portfolio
  CNAME             points GitHub Pages at srishtigangolly.com
archive/            old drafts and source images, not published
.github/workflows/  the deploy workflow
```
