# SusiElectronics — Official Website

> **Trusted Service. Genuine Care. Smarter Living.**
> Salem's most trusted home appliance sales & service center. Est. 2010.

---

## 📋 Project Overview

This is the official website for **SusiElectronics**, owned by **G Giritharan**, Salem, Tamil Nadu, India. The site is a premium, production-ready static HTML website designed to convert visitors into service bookings — with a cinematic dark UI, smooth animations, and full SEO optimization.

---

## 📁 File Structure

```
SusiElectronics/
│
├── index.html          → Home page (main entry point)
├── about.html          → About us & owner story
├── services.html       → All service detail pages
├── products.html       → Products for sale
├── gallery.html        → Photo gallery (masonry)
├── videos.html         → Video showcase
├── testimonials.html   → Customer reviews
├── faq.html            → Frequently asked questions
├── blog.html           → Blog / tips articles
├── contact.html        → Contact & booking form
├── privacy.html        → Privacy policy
├── terms.html          → Terms of service
├── 404.html            → Custom error page
│
├── sitemap.xml         → XML sitemap for search engines
├── robots.txt          → Crawler instructions
├── manifest.json       → PWA manifest (app install)
├── README.md           → This file
│
├── assets/
│   ├── css/            → Stylesheets (if extracted)
│   ├── js/             → JavaScript files (if extracted)
│   ├── images/         → Photos, icons, og-image
│   ├── videos/         → Local video files
│   └── fonts/          → Custom/local fonts
```

---

## 🚀 Getting Started

### No build step required.
This is a pure HTML/CSS/JS project. Just open `index.html` in any browser.

```bash
# Option 1 — Open directly
open index.html

# Option 2 — Local dev server (recommended)
npx serve .

# Option 3 — Python quick server
python3 -m http.server 8080
# Then visit: http://localhost:8080
```

---

## ✅ Before Going Live — Checklist

### 1. Replace Placeholder Phone Number
Search and replace `+919876543210` in all HTML files with the real business number.

```
Find:    +919876543210
Replace: [actual phone number]
```

Also update the WhatsApp links:
```
Find:    https://wa.me/919876543210
Replace: https://wa.me/91[actual number]
```

### 2. Update Domain Name
In `sitemap.xml` and `robots.txt`, replace the placeholder domain:
```
Find:    https://susielectronics.in
Replace: https://[your-actual-domain.com]
```

### 3. Add Real Address
In `index.html` and `contact.html`, update the address section with the full shop address including street, pincode.

### 4. Embed Google Maps
In the contact section, replace the map placeholder with a real Google Maps embed:
```html
<!-- Replace the .contact-map div content with: -->
<iframe
  src="https://www.google.com/maps/embed?pb=YOUR_EMBED_URL"
  width="100%" height="200" style="border:0;" allowfullscreen
  loading="lazy">
</iframe>
```
Get your embed URL from: **Google Maps → Share → Embed a map**

### 5. Add Real Images
Place images in `assets/images/` and reference them in the HTML:
- `og-image.jpg` — 1200×630px (for social sharing previews)
- `favicon.ico` / `favicon.png` — 32×32px and 180×180px
- Service photos, team photos, gallery images

### 6. Add Favicon
```html
<!-- Add inside <head> of every HTML file -->
<link rel="icon" type="image/png" href="assets/images/favicon.png">
<link rel="apple-touch-icon" href="assets/images/apple-touch-icon.png">
```

### 7. Email / WhatsApp Form Integration
The booking form currently opens WhatsApp with a pre-filled message. To also send email notifications, integrate **EmailJS**:
1. Sign up at [emailjs.com](https://www.emailjs.com)
2. Create a service and email template
3. Add your `service_id`, `template_id`, and `public_key` to the form's submit handler in `index.html`

### 8. Google Analytics
Add your GA4 tracking code inside `<head>` on every page:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### 9. Google Search Console
After deploying:
1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Add your domain and verify ownership
3. Submit: `https://yourdomain.com/sitemap.xml`

---

## 🎨 Design System

| Token | Value | Usage |
|---|---|---|
| `--bg-void` | `#07070E` | Page background |
| `--accent-cyan` | `#00D4FF` | Primary accent, CTAs |
| `--accent-violet` | `#7B2FBE` | Gradient pair, highlights |
| `--accent-ember` | `#FF6B35` | Emergency, alerts |
| `--text-ice` | `#F0F4FF` | Headings, primary text |
| `--text-muted` | `rgba(240,244,255,0.55)` | Body text |
| `--text-dim` | `rgba(240,244,255,0.35)` | Labels, captions |

**Fonts used:**
- `Syne` — Display headings (Google Fonts)
- `Inter` — Body text (Google Fonts)
- `JetBrains Mono` — Stats, labels, code (Google Fonts)

---

## ⚡ Performance Notes

- All CSS and JS is inline in `index.html` — zero extra HTTP requests
- Images should be converted to **WebP** format for best performance
- Use `loading="lazy"` on all `<img>` tags below the fold
- Fonts are loaded via `preconnect` to Google Fonts for faster rendering
- Animations respect `prefers-reduced-motion` — accessible by default

---

## 📱 Responsive Breakpoints

| Breakpoint | Target |
|---|---|
| `> 1024px` | Desktop & laptop |
| `768px – 1024px` | Tablet |
| `480px – 768px` | Mobile |
| `< 480px` | Small mobile |

---

## 🔍 SEO Features

- ✅ Semantic HTML5 structure (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- ✅ JSON-LD `LocalBusiness` schema (in `<head>` of `index.html`)
- ✅ OpenGraph meta tags for social sharing
- ✅ Twitter Card meta tags
- ✅ Canonical URL tag
- ✅ `sitemap.xml` with all pages
- ✅ `robots.txt` with sitemap reference
- ✅ Target keywords naturally embedded in content:
  - "AC service Salem"
  - "Refrigerator repair Salem"
  - "Washing machine repair Salem"
  - "Appliance service Salem Tamil Nadu"

---

## 🌐 Deployment Options

### Option A — Shared Hosting (cPanel)
1. Zip the entire project folder
2. Upload via File Manager to `public_html/`
3. Extract and ensure `index.html` is at root

### Option B — Netlify (Free, Recommended)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop the project folder
3. Your site goes live instantly with HTTPS

### Option C — GitHub Pages (Free)
1. Push the project to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Site will be live at `https://username.github.io/repo-name`

### Option D — Vercel (Free)
```bash
npm i -g vercel
vercel
```

---

## 📞 Business Information

| Field | Details |
|---|---|
| Business Name | SusiElectronics |
| Owner | G Giritharan |
| Location | Salem, Tamil Nadu, India |
| Established | 2010 |
| Operating Hours | 24 Hours / 7 Days |
| Services | AC, Refrigerator, Washing Machine, LED TV, RO Purifier, Air Cooler, Microwave |

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Markup & structure |
| CSS3 (custom properties) | Styling & design system |
| Vanilla JavaScript (ES2025) | Interactions & animations |
| Google Fonts | Typography (Syne, Inter, JetBrains Mono) |
| IntersectionObserver API | Scroll reveal animations |
| CSS animations | Aurora, float, marquee, pulse effects |
| JSON-LD | Structured data / SEO schema |
| WhatsApp API | Booking form integration |

---

## 📄 License

This website was custom-built for **SusiElectronics, Salem**. All rights reserved © 2025 SusiElectronics. Unauthorized reproduction or redistribution is not permitted.

---

*Built with care for Salem's most trusted appliance service center.*
