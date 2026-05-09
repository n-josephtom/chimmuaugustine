# Alexandra Reyes — Content Writer Portfolio

A production-ready, dark editorial portfolio website for a content writer and content marketing specialist. Includes an inline PDF resume viewer.

## 📁 Project Structure

```
portfolio/
├── index.html       ← Full single-page portfolio site
├── resume.pdf       ← Resume (viewable inline, no download needed)
├── vercel.json      ← Vercel deployment config (serves PDF inline)
└── README.md
```

## 🚀 Deploy to Vercel (Free)

### Option A — Vercel CLI (Recommended)

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Login
vercel login

# 3. Deploy from the portfolio folder
cd portfolio
vercel

# 4. Follow prompts — select "No" for existing project, use defaults
# Your site will be live at https://your-project.vercel.app
```

### Option B — GitHub + Vercel Dashboard

1. Push this folder to a GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio deploy"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

2. Go to [vercel.com](https://vercel.com) → **New Project**

3. Import your GitHub repository

4. Leave all settings as default (Framework: **Other**, Root directory: `.`)

5. Click **Deploy** — your site is live in ~30 seconds ✅

## ✏️ Customisation Checklist

Open `index.html` and update the following:

| Item | Location |
|------|----------|
| **Your Name** | `<title>`, `.nav-logo`, `.hero-name`, footer |
| **Your Title** | Hero tagline, `<meta description>` |
| **Stats** (years, clients, traffic %) | `.hero-stats` section |
| **Services Offered** | `.service-pill` tags and `.services-grid` cards |
| **Portfolio Projects** | `#portfolio` section — update titles, descriptions, metrics |
| **Testimonials** | `#testimonials` section |
| **Contact Info** | `#contact` section — email, LinkedIn, Twitter |
| **Social Links** | `.contact-link` elements |

### Replace the Resume PDF

1. Replace `resume.pdf` with your own PDF file (keep the same filename), OR
2. Update every `src="resume.pdf"` and `href="resume.pdf"` reference in `index.html` to your new filename.

## 🖨️ PDF Viewer Notes

The resume is displayed inline using the browser's native `<embed>` tag — no library needed:
- ✅ Chrome / Edge — full PDF toolbar, zoom, scroll
- ✅ Firefox — native PDF viewer
- ✅ Safari (desktop) — native viewer  
- 📱 Mobile (iOS/Android) — falls back to a styled "Open PDF" button (PDF.js isn't needed for Vercel/static hosting)

The `vercel.json` sets `Content-Disposition: inline` so the browser displays rather than downloads the PDF by default.

## 🎨 Colour Palette

| Variable | Hex | Use |
|----------|-----|-----|
| `--navy` | `#0d1b2a` | Background |
| `--gold` | `#c9a84c` | Primary accent |
| `--coral` | `#e8715a` | Secondary accent |
| `--cream` | `#f4ede0` | Headings / light text |
| `--muted` | `#7a9ab8` | Body text |

## 📄 Licence

Feel free to adapt this for your own portfolio. Not for resale.
