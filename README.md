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

Edit **`_data/team.yml`** and add a new entry at the bottom. Copy this template and fill in the details:

```yaml
- name: "First Last"
  title: "Research Assistant"
  photo: "lastname.webp"
  group: "research_assistants"
  bio: "Write the bio here. Keep it all on one line."
```

For `group`, use `"leadership"` or `"research_assistants"`.

Then upload their photo:
1. Go to **`assets/images/team/`**
2. Click **Add file > Upload files**
3. Name the file to match the `photo` field above (e.g., `lastname.webp`)

To **remove** a team member, delete their block (from the `-` to the line before the next `-`).

---

## Adding a Publication

Edit **`_data/publications.yml`** and add a new entry at the **top** of the file:

```yaml
- citation: "Author, A., Author, B. (2026). Title of paper. Journal Name, volume(issue), pages."
  doi: "https://doi.org/your-doi-here"
```

That's it — the citation text and the DOI link. The site handles the formatting.

---

## Adding a Resource

Edit **`_data/resources.yml`** and add a new entry at the bottom:

```yaml
- name: "Resource Name"
  url: "https://example.com"
  description: "What this resource offers."
```

If the resource has a phone number, add a `phone` line:

```yaml
- name: "Resource Name"
  url: "https://example.com"
  description: "What this resource offers."
  phone: "Helpline: 800-123-4567"
```

If there's no website, leave `url` empty: `url: ""`

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

Pages like About, Participate, and Contact are in the **`_pages/`** folder:

| File | Page |
|---|---|
| `about.md` | About |
| `participate.md` | Participate |
| `contact-us.md` | Contact |

The homepage is `index.html` in the root folder.

Team, Publications, and Resources are managed through the data files described above — you don't need to touch the page templates.

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

## Important: YAML Formatting Tips

The data files (`_data/*.yml`) are sensitive to formatting. Follow these rules:

- Each entry starts with `- ` (dash + space)
- Fields are indented with **two spaces** (not tabs)
- Wrap all values in `"double quotes"`
- Keep bios on **one line** — no line breaks inside the quotes
- Don't change the field names (`name:`, `title:`, `bio:`, etc.)

If the site doesn't build after your edit, you probably have a formatting issue. Check for missing quotes or wrong indentation.

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
