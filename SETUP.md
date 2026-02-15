# GitHub Pages Setup Instructions

This guide shows you how to host your Advanced Search & Bulk Actions documentation on GitHub Pages for free.

## Prerequisites

- GitHub account (free)
- Git installed on your computer (optional, can use GitHub web interface)

## Option 1: Using GitHub Web Interface (Easiest)

### Step 1: Create a New Repository

1. Go to [GitHub.com](https://github.com) and log in
2. Click the **"+"** icon (top right) → **"New repository"**
3. **Repository name:** `advanced-search-docs` (or any name you prefer)
4. **Description:** "Help documentation for Advanced Search & Bulk Actions"
5. Set to **Public** (required for free GitHub Pages)
6. ✅ Check **"Add a README file"**
7. Click **"Create repository"**

### Step 2: Upload Documentation Files

1. In your new repository, click **"Add file"** → **"Upload files"**
2. Drag and drop ALL files from your `advanced-search-docs` folder:
   - README.md
   - _config.yml
   - images/ folder (with all screenshots)
   - docs/ folder (with all .md files)
3. Add commit message: "Initial documentation upload"
4. Click **"Commit changes"**

### Step 3: Enable GitHub Pages

1. In your repository, click **"Settings"** tab
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Source"**, select:
   - Branch: **main** (or master)
   - Folder: **/ (root)**
4. Click **"Save"**
5. Wait 1-2 minutes for GitHub to build your site

### Step 4: Access Your Documentation

Your docs will be available at:
```
https://YOUR-USERNAME.github.io/advanced-search-docs/
```

Replace `YOUR-USERNAME` with your GitHub username.

**Example:** If your username is `johndoe`:
```
https://johndoe.github.io/advanced-search-docs/
```

---

## Option 2: Using Git Command Line

### Step 1: Create Repository on GitHub

1. Go to [GitHub.com](https://github.com) → New repository
2. Name: `advanced-search-docs`
3. Set to **Public**
4. Do NOT initialize with README
5. Click **"Create repository"**

### Step 2: Upload via Git

Open terminal in your `advanced-search-docs` folder:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial documentation upload"

# Add remote (replace YOUR-USERNAME)
git remote add origin https://github.com/YOUR-USERNAME/advanced-search-docs.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

Same as Option 1, Step 3 above.

---

## Customizing Your Docs

### Change Theme

Edit `_config.yml` and change the theme line:

```yaml
# Available themes:
theme: jekyll-theme-minimal
theme: jekyll-theme-cayman       # Current (default)
theme: jekyll-theme-slate
theme: jekyll-theme-architect
theme: jekyll-theme-midnight
```

[View all themes](https://pages.github.com/themes/)

### Update Documentation

To update your docs:

**Via Web Interface:**
1. Navigate to the file you want to edit
2. Click the pencil (✏️) icon
3. Make changes
4. Commit changes

**Via Git:**
```bash
# Make your changes locally
git add .
git commit -m "Updated documentation"
git push
```

Changes appear on your site within 1-2 minutes.

### Add Custom Domain (Optional)

If you own a domain:

1. In repository settings → Pages
2. Under "Custom domain", enter your domain
3. Follow GitHub's instructions to configure DNS
4. Enable "Enforce HTTPS"

---

## Folder Structure

Your repository should look like this:

```
advanced-search-docs/
├── README.md                    # Homepage
├── _config.yml                  # GitHub Pages config
├── SETUP.md                     # This file
├── images/                      # Screenshots
│   ├── 01-main-interface.png
│   ├── 02-search-results.png
│   ├── 03-entity-selector.png
│   ├── 04-action-buttons.png
│   ├── 05-bulk-changes.png
│   ├── 06-saved-searches.png
│   ├── 07-export-options.png
│   └── 08-filters.png
└── docs/                        # Documentation pages
    ├── getting-started.md
    ├── searching.md
    ├── bulk-actions.md
    ├── saved-searches.md
    ├── exporting.md
    └── faq.md
```

## Linking to Your Docs

### From Your Zendesk App

In your app's "Get Help" button, link to:
```
https://YOUR-USERNAME.github.io/advanced-search-docs/
```

### In App Manifest

Add to `manifest.json`:
```json
{
  "supportUrl": "https://YOUR-USERNAME.github.io/advanced-search-docs/"
}
```

### In README or Marketing

```markdown
[View Documentation](https://YOUR-USERNAME.github.io/advanced-search-docs/)
```

---

## Troubleshooting

### Site Not Loading

**Possible causes:**
- GitHub Pages not enabled in settings
- Repository is private (must be public)
- Waiting for initial build (takes 1-2 minutes)

**Solutions:**
- Check Settings → Pages is configured
- Make repository public
- Wait a few minutes and refresh

### Images Not Showing

**Possible causes:**
- Image paths incorrect
- Images not uploaded
- Case sensitivity (image.png vs Image.PNG)

**Solutions:**
- Verify images are in `images/` folder
- Check image references in markdown: `![Alt](../images/filename.png)`
- Use lowercase filenames

### Theme Not Applied

**Possible causes:**
- `_config.yml` not in root directory
- Invalid theme name
- Waiting for rebuild

**Solutions:**
- Ensure `_config.yml` is in repository root
- Use valid Jekyll theme names
- Wait 1-2 minutes for rebuild

### Links Broken

**Possible causes:**
- Incorrect relative paths
- Missing `.md` extensions
- Case sensitivity

**Solutions:**
- Use relative paths: `./docs/getting-started.md`
- Include file extensions
- Match exact case of filenames

---

## Next Steps

After setting up GitHub Pages:

1. ✅ Test all links on your live site
2. ✅ Verify all images load correctly
3. ✅ Update "Get Help" button in your app to point to docs
4. ✅ Share docs URL with your team
5. ✅ Keep documentation updated as app evolves

---

## Advanced: Custom Styling (Optional)

To add custom CSS:

1. Create `assets/css/style.scss` in your repository:

```scss
---
---

@import "{{ site.theme }}";

/* Your custom styles */
.main-content {
  max-width: 900px;
}

h1 {
  color: #0F7CC0; /* Zendesk blue */
}

img {
  border: 1px solid #ddd;
  border-radius: 4px;
  margin: 20px 0;
  max-width: 100%;
}
```

2. Commit and push
3. Custom styles apply automatically

---

## Questions?

If you need help with GitHub Pages:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)

---

**Your documentation is ready to go live! 🚀**
