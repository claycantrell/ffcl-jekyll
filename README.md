# FFCL Website

Website for the Falzarano Family Caregiving Lab. Built with Jekyll, hosted on GitHub Pages.

**Live site:** https://claycantrell.github.io/ffcl-jekyll/

---

## Editing Content

All content lives in simple text files. You don't need to install anything — you can edit files directly on GitHub.

### How to edit a page

1. Go to the `_pages/` folder on GitHub
2. Click the file you want to edit (e.g., `about.md`)
3. Click the pencil icon (Edit this file)
4. Make your changes
5. Click **Commit changes** at the bottom
6. The site will automatically rebuild in about a minute

### Page files

| File | Page |
|---|---|
| `index.html` | Homepage |
| `_pages/about.md` | About |
| `_pages/participate.md` | Participate |
| `_pages/our-team.md` | Our Team |
| `_pages/resources.md` | Resources |
| `_pages/publications.md` | Publications |
| `_pages/contact-us.md` | Contact |

### Writing format

Pages use **Markdown**, a simple formatting syntax:

```markdown
# Big Heading
## Smaller Heading
### Even Smaller Heading

Regular paragraph text goes here.

**Bold text**
*Italic text*

- Bullet point
- Another bullet point

[Link text](https://example.com)
```

---

## Adding a New Page

1. Go to `_pages/` on GitHub
2. Click **Add file > Create new file**
3. Name it something like `new-page.md`
4. Start the file with this header (change the title and permalink):

```markdown
---
layout: page
title: Your Page Title
permalink: /your-page-url/
---

# Your Page Title

Your content goes here.
```

5. Commit the file
6. To add it to the navigation, edit `_includes/nav.html` and add a new `<li>` entry following the pattern of the existing links

---

## Adding / Replacing Photos

### Team photos

1. Go to `assets/images/team/` on GitHub
2. Click **Add file > Upload files**
3. Name the photo after the person's last name (e.g., `smith.webp` or `smith.jpg`)
4. Edit `_pages/our-team.md` and update the `src` path in the team member's card to match the new filename

### Partner logos

1. Upload to `assets/images/partners/`
2. Edit `index.html` and update the partner logo section

### Photo carousel

1. Upload to `assets/images/photos/`
2. Photos are named `photo1.jpg` through `photo8.jpg`
3. To replace one, upload a new file with the same name
4. To add more, upload `photo9.jpg` etc. and update the loop in `index.html` from `(1..8)` to `(1..9)`

---

## Adding a Publication

Edit `_pages/publications.md` and add a new entry at the top of the list:

```markdown
- Author, A., Author, B. (2026). Title of the paper. *Journal Name*, volume(issue), pages. [DOI](https://doi.org/your-doi-here)
```

---

## Adding a Resource

Edit `_pages/resources.md` and add a new block inside the `<div class="resources-list">`:

```html
<div class="resource-item">
<h3><a href="https://example.com" target="_blank">Resource Name</a></h3>
<p>Description of the resource.</p>
</div>
```

---

## Colors

The site uses these colors, defined in `_sass/main.scss`:

| Color | Hex | Use |
|---|---|---|
| Black | `#000000` | Page background |
| Red | `#990000` | Accents, section headers, borders |
| White | `#ffffff` | Partner section, headings |
| Light grey | `#dddddd` | Body text |

---

## Running Locally (optional)

If you want to preview changes on your computer before pushing:

```bash
# Requires Ruby 3+
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```

Most people won't need this — just edit on GitHub and the site updates automatically.
