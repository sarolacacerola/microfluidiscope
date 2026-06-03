# microfluidoscope

## File Structure

```
/
├── index.html              ← Landing page
├── css/
│   └── style.css           ← All styles
├── js/
│   └── main.js             ← Nav, scroll reveal, contact form
├── images/                 ← Add your images here
│   └── (your images)
└── pages/
    ├── component-a.html    ← Component A build docs
    ├── component-b.html    ← Component B build docs
    ├── component-c.html    ← Component C build docs
    ├── workshops.html      ← Workshops & tutorials
    └── contact.html        ← Contact form + team
```

## Customising the content

### 1. Rename everything
Search and replace `MakerKit` with your product name across all files.
Update `your-org/makerkit` GitHub links to your actual repo.

### 2. Hero image
In `index.html`, find `.hero-image-placeholder` and replace with:
```html
<div class="hero-image-placeholder">
  <img src="images/your-product.jpg" alt="Your product name" style="width:100%; height:100%; object-fit:cover;">
</div>
```

### 3. Component pages
Each component page (`component-a.html`, `component-b.html`, `component-c.html`) has placeholder text throughout. Replace:
- Page title and description
- Overview text
- Bill of Materials list
- Build steps
- GitHub repo links

Rename the files and update all nav links if you want different names.

### 4. Partner logos
In `index.html`, find the `.partners-grid` section. Replace each `.partner-logo` div with:
```html
<div class="partner-logo">
  <img src="images/partner-name.png" alt="Partner Name" style="max-height: 50px; max-width: 140px; object-fit: contain;">
</div>
```

### 5. Team photos
In `contact.html`, replace each `👤` emoji in `.team-avatar` with:
```html
<img src="../images/name.jpg" alt="Name" style="width:100%; height:100%; border-radius:50%; object-fit:cover;">
```

### 6. Contact form
The form is wired for [Formspree](https://formspree.io) (free tier available). Sign up, create a form, then in `contact.html` update:
```html
<form id="contactForm" class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### 7. Workshop cards
In `workshops.html`, edit or duplicate `.workshop-card` blocks for each session. Update date, location, and time in `.workshop-meta`.

---

## Deploy on Cloudflare Pages

1. Push this repo to GitHub
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/)
3. Connect your GitHub account → select this repo
4. Build settings:
   - **Framework preset**: None
   - **Build command**: (leave blank)
   - **Build output directory**: `/` (root)
5. Deploy — Cloudflare will give you a `.pages.dev` URL instantly
6. Add a custom domain in the Cloudflare Pages dashboard under Settings → Custom Domains

---

## Deploy on GitHub Pages

1. Go to repo Settings → Pages
2. Source: Deploy from branch → `main` → `/ (root)`
3. Your site will be live at `https://your-org.github.io/makerkit`
