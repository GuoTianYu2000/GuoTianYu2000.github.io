# Tianyu Guo — Personal Homepage

Source for [guotianyu2000.github.io](https://guotianyu2000.github.io).

## Deploying to GitHub Pages

### One-time setup

1. **Create the repository** on GitHub named exactly `GuoTianYu2000.github.io`
   - Go to https://github.com/new
   - Repository name: `GuoTianYu2000.github.io`
   - Set to **Public**

2. **Push from this folder**
   ```bash
   cd /Users/tianyu_guo/Github/homepage
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin git@github.com:GuoTianYu2000/GuoTianYu2000.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages** (usually auto-enabled for `username.github.io` repos)
   - Go to the repo → Settings → Pages
   - Source: Deploy from branch → `main` → `/ (root)`
   - Your site will be live at **https://guotianyu2000.github.io** within a minute or two.

## Customizing

### Add your profile photo
1. Save your photo as `assets/img/profile.jpg`
2. In `index.html`, replace the placeholder block:
   ```html
   <!-- Replace this: -->
   <div class="profile-photo-placeholder" aria-hidden="true">👤</div>

   <!-- With this: -->
   <img class="profile-photo" src="assets/img/profile.jpg" alt="Tianyu Guo" />
   ```

### Add your CV
1. Place your CV PDF as `cv.pdf` in the root folder
2. In `index.html`, uncomment the CV link in the profile links section and the nav

### Update your email
Search for `tianyuguo@berkeley.edu` in `index.html` and update to your actual address.

### Update publications
Publications are listed in `index.html` inside `<ul class="pub-list">`.
Each paper follows this template:
```html
<li class="pub-item">
  <span class="pub-number">N</span>
  <div class="pub-content">
    <div class="pub-title">
      <a href="PAPER_URL">Paper Title</a>
    </div>
    <div class="pub-authors">
      Author 1, <strong>T. Guo</strong>, Author 3
    </div>
    <div class="pub-venue">
      <span class="venue-name">Venue Name</span>, Year
    </div>
    <div class="pub-badges">
      <span class="badge badge-conf">Conference</span>
      <a class="badge-link" href="PAPER_URL">[Paper]</a>
    </div>
  </div>
</li>
```

Badge classes available: `badge-arxiv`, `badge-conf`, `badge-journal`

## File structure

```
homepage/
├── index.html          # Main page (edit this)
├── assets/
│   ├── css/
│   │   └── main.css    # All styles
│   └── img/
│       └── profile.jpg # Your photo (add this)
├── cv.pdf              # Your CV (add this)
└── README.md
```
