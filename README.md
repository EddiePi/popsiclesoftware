# MyBrand Website

A clean, multi-page static website ready to host on **GitHub Pages**.

## File Structure

```
├── index.html              ← Home / Welcome page
├── css/
│   └── style.css           ← Shared styles for all pages
├── js/
│   └── nav.js              ← Shared nav highlighting script
└── pages/
    ├── product1.html       ← Product 1 page
    ├── product2.html       ← Product 2 page (same layout as product1)
    └── privacy.html        ← Privacy Policy page
```

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `mybrand-site`)
2. Push all files to the `main` branch
3. Go to **Settings → Pages**
4. Under *Source*, select **Deploy from a branch**
5. Choose **main** branch and **/ (root)** folder
6. Click **Save** — your site will be live at `https://<your-username>.github.io/<repo-name>/`

## Customising the Site

### Rename the brand
Search and replace `MyBrand` across all HTML files with your actual brand name.

### Edit page content
- **Home:** edit `index.html` — update the hero headline, description, and product cards
- **Products:** edit `pages/product1.html` and `pages/product2.html` — replace placeholder text and feature tiles
- **Privacy:** edit `pages/privacy.html` — update dates, contact email, and policy details

### Adding a new product page

1. Copy `pages/product1.html` → `pages/product3.html`
2. Update the `<title>`, `<h1>`, and all placeholder content inside
3. Add a nav link in **every** HTML file:
   ```html
   <li><a href="pages/product3.html">Product 3</a></li>   <!-- in index.html -->
   <li><a href="product3.html">Product 3</a></li>          <!-- in pages/*.html -->
   ```
4. Add a product card to the grid in `index.html`

### Changing colours / fonts
All design tokens live at the top of `css/style.css`:
```css
:root {
  --ink:    #1a1a2e;   /* dark background */
  --cream:  #f5f0e8;   /* light background */
  --accent: #c8783a;   /* brand colour */
  --muted:  #7a7a8c;   /* body text */
}
```
