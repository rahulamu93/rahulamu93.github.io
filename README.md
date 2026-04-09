# Rahul Singh — Personal Portfolio Website

This is Rahul Singh's personal portfolio website, hosted for free on **GitHub Pages**. It showcases your background, resume, projects, publications, and contact information.

🌐 **Live site:** [https://rahulamu93.github.io](https://rahulamu93.github.io)

---

## Table of Contents

1. [How to Edit Online (Recommended)](#how-to-edit-online-recommended)
2. [How to Edit Content](#how-to-edit-content)
3. [How to Change Photos](#how-to-change-photos)
4. [How to Change Links](#how-to-change-links)
5. [How to Remove a Section](#how-to-remove-a-section)
6. [How to Save Changes](#how-to-save-changes)
7. [File Structure](#file-structure)
8. [Tips & Troubleshooting](#tips--troubleshooting)

---

## How to Edit Online (Recommended)

You don't need to install anything on your computer. GitHub provides a free online editor called **Codespaces** that works right in your web browser.

1. Go to your repository: [https://github.com/rahulamu93/rahulamu93.github.io](https://github.com/rahulamu93/rahulamu93.github.io)
2. Click the green **Code** button (near the top right)
3. Click the **Codespaces** tab
4. Click **Create codespace on main**
5. Wait about a minute — it will open an editor (VS Code) right in your browser
6. You can now edit any file. When you're done, save your changes (see [How to Save Changes](#how-to-save-changes))

> **Tip:** You can also make quick edits by clicking any file on GitHub and pressing the ✏️ pencil icon to edit it directly.

---

## How to Edit Content

All of the website's text lives in **one file**: `index.html`. Open it and use **Ctrl+F** (or **Cmd+F** on Mac) to search for the text you want to change.

### Change Your Name or Title

Search for `Rahul Singh` to find the name. It appears in a few places — update each one.

Search for `PhD Researcher & Motor Control Engineer` to change the job title that appears below your name.

### Change the About Text

Search for `About me`. Just below it you'll find two paragraphs (`<p>...</p>`) describing your background. Replace the text between `<p>` and `</p>` with your new text.

```html
<p>
  Your new bio text goes here.
</p>
```

### Change Contact Info

Search for these to find and update each contact detail:

| What to change | Search for | What to edit |
|---|---|---|
| Email | `singh.67@iitj.ac.in` | Replace with your new email (appears twice — in `href="mailto:..."` and in the visible text) |
| Phone | `+917275915933` | Replace with your new number (appears twice — in `href="tel:..."` and in the visible text) |
| Birthday | `July 01, 1993` | Replace the date text |
| Location | `IIT Jodhpur, Rajasthan, India` | Replace with your new location |

### Edit the Resume Section

Search for `Resume` to find this section. It has three parts:

- **Education** — Search for `Education`. Each degree is inside a `<li class="timeline-item">` block. Edit the degree name, years, and description.
- **Experience** — Search for `Experience`. Same structure as Education — edit job titles, dates, and descriptions.
- **Skills** — Search for `My skills`. Each skill has a name and a percentage. Change the skill name inside `<h5>` tags and the percentage in both the `value="90"` and `style="width: 90%;"` parts.

### Edit the Portfolio / Projects Section

Search for `Portfolio`. Each project is a `<li class="project-item">` block containing:
- A project image (the `<img src="...">` part)
- A project title (inside `<h3 class="project-title">`)
- A category — either `Research` or `Projects` (inside `<p class="project-category">`)

To add a new project, copy an existing `<li class="project-item">...</li>` block and paste it right after the last one, then change the details.

### Edit the Publications Section

Search for `Publications`. Each publication is a `<li class="blog-post-item">` block containing:
- A link (the `<a href="...">` part — put the DOI or paper URL here)
- An image
- A category (e.g., `IEEE Conference`, `Elsevier Journal`)
- A date
- A title and description

### Edit the Contact Section

Search for `Contact Form`. The form has fields for name, email, and message. The embedded Google Map is just above it — search for `google.com/maps/embed` to change the map location.

---

## How to Change Photos

All images are stored in the `assets/images/` folder.

### Replace Your Profile Photo

1. Name your new photo `my-avatar.png`
2. Put it in the `assets/images/` folder (replacing the old one)
3. That's it — the website will automatically use the new photo

> If your new photo has a different filename (e.g., `photo.jpg`), search for `my-avatar.png` in `index.html` and replace it with your new filename.

### Replace Project Thumbnails

Project images are named `project-1.jpg`, `project-2.png`, etc. in `assets/images/`.

- **Easiest way:** Name your new image the same as the old one and replace it in the folder.
- **Different filename:** Search for the old filename (e.g., `project-1.jpg`) in `index.html` and replace it with the new one.

Publication images follow the same pattern with names like `blog-1.jpg`, `blog-2.jpg`, etc.

---

## How to Change Links

### Social Media Links

Search for `social-link` in `index.html`. You'll find a block like this:

```html
<a href="https://www.linkedin.com/in/rahul-singh-2b5bb8b5/" class="social-link">
```

Replace the URL inside `href="..."` with your new link. To add another social link (e.g., GitHub), copy the entire `<li class="social-item">...</li>` block and change the URL and icon name.

### Project & Publication Links

Each project and publication has an `<a href="...">` tag. Search for the current URL (or `href="#"` for placeholder links) and replace it with the real link.

---

## How to Remove a Section

Each section of the website is wrapped in an `<article>` tag with a clear comment above it. For example:

```html
<!--
  - #PORTFOLIO
-->
<article class="portfolio" data-page="portfolio">
  ...everything in this section...
</article>
```

To remove a section:

1. Find the comment (e.g., `#PORTFOLIO`)
2. Select everything from the comment down to and **including** the closing `</article>` tag
3. Delete it all
4. Also remove the matching navigation button in the `<nav class="navbar">` section (search for the section name like `Portfolio`)

⚠️ **Be careful:** Make sure you delete the **complete** block — from the opening `<article>` to the closing `</article>`. Deleting only part of it will break the page.

---

## How to Save Changes

After editing files in Codespaces:

1. Click the **Source Control** icon in the left sidebar (it looks like a branch/fork symbol, and may show a number badge)
2. You'll see a list of changed files
3. Type a short description of what you changed in the **Message** box (e.g., "Updated bio text")
4. Click the **✓ checkmark** button (or press **Ctrl+Enter**) to commit
5. Click **Sync Changes** when prompted

Your changes will go live on the website automatically — it usually takes **1–2 minutes** for GitHub Pages to update.

---

## File Structure

| File / Folder | What it does |
|---|---|
| `index.html` | **All website content** — text, sections, links. This is the main file you'll edit. |
| `assets/css/style.css` | Controls colors, fonts, spacing, and layout. |
| `assets/js/script.js` | Makes interactive features work (navigation tabs, filters). |
| `assets/images/` | All photos — profile picture, project thumbnails, publication images. |

---

## Tips & Troubleshooting

- **Preview before publishing:** In Codespaces, right-click `index.html` and choose "Open with Live Server" (if available) to preview changes before saving.
- **Something broke?** Don't panic. Go to your repository on GitHub, click **Commits**, find the last working version, and click **Revert** to undo your changes.
- **Don't delete files you're unsure about.** If you're not sure what a file does, leave it alone. Deleting `style.css` or `script.js` will break the site's appearance or interactivity.
- **Editing tip:** Always use **Ctrl+F** / **Cmd+F** to search for the exact text you want to change — it's much faster than scrolling through the file.
- **Need help?** HTML tags are the words inside angle brackets like `<p>` and `</p>`. Your actual content goes *between* them. Don't delete the tags themselves — just change the text between them.
