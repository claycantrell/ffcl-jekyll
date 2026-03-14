# FFCL Website

Website for the Falzarano Family Caregiving Lab. Built with Jekyll, hosted on GitHub Pages.

**Live site:** https://claycantrell.github.io/ffcl-jekyll/

---

## How to Make Changes

All changes are made directly on GitHub — no software to install. Edit a file, click commit, and the site updates automatically in about a minute.

1. Go to the file you want to edit (see sections below)
2. Click the **pencil icon** (Edit this file)
3. Make your changes
4. Click **Commit changes** at the bottom
5. Done — the site rebuilds automatically

---

## Adding a Team Member

Edit **`_pages/our-team.md`** and copy/paste this block inside the `<div class="team-grid">` section:

```html
<div class="team-card">
  <img src="{{ '/assets/images/team/LASTNAME.webp' | relative_url }}" alt="FULL NAME" class="team-photo">
  <h3 class="team-name">FULL NAME</h3>
  <p class="team-title">TITLE (e.g., Research Assistant)</p>
  <p class="team-bio">BIO TEXT GOES HERE.</p>
</div>
```

Replace `LASTNAME`, `FULL NAME`, `TITLE`, and `BIO TEXT` with the new member's info.

Then upload their photo:
1. Go to **`assets/images/team/`**
2. Click **Add file > Upload files**
3. Name it `lastname.webp` (or `.jpg`/`.png`) — must match the filename in the code above

To **remove** a team member, delete their `<div class="team-card">...</div>` block.

---

## Adding a Publication

Edit **`_pages/publications.md`** and add a new line at the **top** of the list (right after the `<div>` tag):

```markdown
- Author, A., Author, B. (2026). Title of the paper. *Journal Name*, volume(issue), pages. [DOI](https://doi.org/your-doi-here)
```

Wrap the journal name in `*asterisks*` to italicize it. The `[DOI](url)` part creates a clickable link.

---

## Adding a Resource

Edit **`_pages/resources.md`** and add this block inside the `<div class="resources-list">`:

```html
<div class="resource-item">
<h3><a href="https://example.com" target="_blank">Resource Name</a></h3>
<p>Description of the resource goes here.</p>
</div>
```

If the resource has a phone number, add it as a separate line:

```html
<p><strong>Helpline: 800-123-4567</strong></p>
```

If there's no website link, just use `<h3>Resource Name</h3>` without the `<a>` tag.

---

## Adding & Replacing Photos

### Team photos

1. Go to **`assets/images/team/`**
2. Click **Add file > Upload files**
3. Name the file after the person's last name (e.g., `smith.webp`)
4. To **replace** an existing photo, upload a new file with the same name

### Photo carousel (homepage)

1. Go to **`assets/images/photos/`**
2. Photos are named `photo1.jpg` through `photo8.jpg`
3. To **replace** one, upload a new file with the same name
4. To **add** more, upload `photo9.jpg` etc. and edit `index.html` — change `(1..8)` to `(1..9)`

### Partner logos (homepage)

1. Upload to **`assets/images/partners/`**
2. Edit `index.html` and update the partner logo section to reference the new file

---

## Editing Page Content

All pages are in the **`_pages/`** folder:

| File | Page |
|---|---|
| `about.md` | About |
| `participate.md` | Participate |
| `our-team.md` | Our Team |
| `resources.md` | Resources |
| `publications.md` | Publications |
| `contact-us.md` | Contact |

The homepage is `index.html` in the root folder.

Pages use **Markdown** formatting:

```
# Big Heading
## Smaller Heading

Regular paragraph text.

**Bold text**
*Italic text*

- Bullet point
- Another bullet point

[Link text](https://example.com)
```

---

## Adding a New Page

1. Go to `_pages/` and click **Add file > Create new file**
2. Name it `your-page.md`
3. Start with this header:

```markdown
---
layout: page
title: Your Page Title
permalink: /your-page-url/
---

# Your Page Title

Content goes here.
```

4. To add it to the navigation bar, edit `_includes/nav.html` and add a new `<li>` entry following the pattern of the existing links

---

## Running Locally (optional)

If you want to preview changes before publishing:

```bash
# Requires Ruby 3+
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```

Most people won't need this — just edit on GitHub and the site updates automatically.
