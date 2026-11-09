# srishti os

The portfolio of Srishti Gangolly, live at **[srishtigangolly.com](https://srishtigangolly.com)**.

It's a retro pixel "operating system": the homepage is a desktop with icons you can open (and drag around), every page is a window, and there's a mailbox where visitors can write a letter or send a bouquet.

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

## How it's built

Plain HTML, CSS and a little JavaScript. No framework and no build step.

- **The mailbox** (`mailbox.html`) is a self-contained page. Letters are posted to [Formspree](https://formspree.io); add `?demo` to the address to try the whole flow without sending anything.
- **Every other page** keeps its markup in a `<template id="page">` with `{{holes}}`, `<sc-if>` and `<sc-for>`, plus a small `class Component` that supplies the values. `js/srishti-os.js` turns that into the live page and re-renders it whenever the component calls `setState()`.
- **Phones** (screens up to 560px wide) get their own tweaks in each page's `@media (max-width:560px)` block: a slightly smaller layout, dropdowns for the bouquet and prompt generator, and hold-to-move icons.
- **Remembered on the visitor's device** (in `localStorage`): icon positions (`srishti-os-icons-v2`), where the welcome window was dragged on a phone (`srishti-os-welcome`) and its width on a computer (`srishti-os-welcome-size`). "tidy up" and double-clicking the window's corner grip reset them.

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

- **Mon Amour font:** the display font isn't uploaded yet, so titles use Fraunces.
- **Share image:** `og.png` (1200×630) for link previews doesn't exist yet.
