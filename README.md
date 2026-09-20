# Elan & ηVision 2027 × Google Sponsorship Proposal

[![Status](https://img.shields.io/badge/Status-Production%20Ready-success?style=flat-square)](#)
[![Theme](https://img.shields.io/badge/Design-Deep%20Violet%20%26%20Gold-8A2BE2?style=flat-square)](#)
[![Engine](https://img.shields.io/badge/Engine-StPageFlip%20v2.0.7-ffb703?style=flat-square)](#)
[![Deployment](https://img.shields.io/badge/Hosting-Cloudflare%20Pages-F38020?logo=cloudflare&style=flat-square)](#)

An interactive, responsive 3D flipbook presentation website created for the **Elan & ηVision 2027** sponsorship proposal to **Google** by the student body of **IIT Hyderabad**, pre-configured for deployment on **Cloudflare Pages**.

---

## ✦ Key Features

- **Realistic 3D Page Flip**: Powered by `St.PageFlip` with realistic paper physics, corner folding, and dynamic shadows.
- **Ambient Festival Stage**: Atmospheric dark-mode backdrop featuring floating canvas particles and glowing rayburst animations.
- **Interactive Sponsorship Tiers**: Instant tabbed switching between Gold (₹2.5L), Platinum (₹5L), and Co-Title (₹10L) deliverables.
- **Branded Mockups & Assets**: High-resolution branded renders for IIT Hyderabad campus entrance arches, main stage LED video walls, and co-branded partnership lockups.
- **Table of Contents & Progress**: Dropdown jump list, animated progress bar, and page index indicator.
- **Responsive & Touch Friendly**: Seamless desktop mouse drag/click support, keyboard navigation (`←`, `→`, `Space`), and mobile responsiveness.
- **Print & PDF Mode**: Fully styled `@media print` layout that renders clean pages when exporting or printing directly to PDF.
- **Enterprise Redundancy**: Ships with a local vendored copy of `page-flip.browser.js` alongside CDN fallback for 100% reliability on restricted corporate intranets.

---

## 📂 Repository Structure

```
├── _headers                      # Cloudflare Pages security & caching headers
├── wrangler.toml                 # Cloudflare Pages deployment configuration
├── assets/
│   ├── favicon/
│   │   └── favicon.svg           # Glowing monogram festival favicon
│   ├── images/
│   │   ├── elan-logo.svg         # Official vector fest emblem
│   │   ├── avatar-shreedhanvi.svg# Sponsorship head verified portrait seal
│   │   ├── festival-highlight.jpg# Night amphitheater crowd & laser highlight
│   │   ├── entrance-arch.jpg     # IIT Hyderabad entrance archway branding mockup
│   │   ├── main-stage-led.jpg    # Main stage curved LED video wall mockup
│   │   ├── cobrand-lockup.jpg    # "Elan & nVision 2027 × Google" lockup graphic
│   │   └── og-preview.jpg        # OpenGraph 1200x630 social share card
│   └── js/
│       └── page-flip.browser.js  # Offline/local flipbook engine
├── .github/
│   └── workflows/
│       └── deploy.yml            # Automated GitHub Pages CI/CD workflow (optional)
├── .gitignore                    # Production exclusions (system, temp, CT dumps)
├── index.html                    # Production-ready main flipbook application
├── package.json                  # Local preview and Cloudflare deployment scripts
└── README.md                     # Documentation & Cloudflare deployment guide
```

> **Note on `log_list.*` files**: The workspace contains `log_list.json` and `log_list.ctfb.html`. These are Chromium Certificate Transparency log dumps that have no relation to the deck, and are cleanly excluded by `.gitignore`.

---

## 🚀 Running Locally

### Option 1: Using Node.js
```bash
# Start a local preview server on port 3000
npm start
```
Then open `http://localhost:3000` in your browser.

### Option 2: Using Python
```bash
python -m http.server 3000
```
Then open `http://localhost:3000` in your browser.

---

## ⚡ Deploying to Cloudflare Pages

### Method 1: Connecting your Git Repository (Recommended)
1. Commit and push this repository to GitHub or GitLab (see [Pushing to Git](#-pushing-to-git) below).
2. Log into the [Cloudflare Dashboard](https://dash.cloudflare.com/) and go to **Compute (Workers) > Workers & Pages > Create application > Pages > Connect to Git**.
3. Select your repository.
4. In the build settings:
   - **Framework preset**: `None`
   - **Build command**: *(leave blank)*
   - **Build output directory**: `.` (or root `/`)
5. Click **Save and Deploy**. Cloudflare Pages will automatically deploy your site on its global edge network with custom SSL.

### Method 2: Direct Deployment via Cloudflare Wrangler CLI
If you want to deploy directly from your local terminal without connecting Git:
```bash
# Deploys directly to Cloudflare Pages using Wrangler
npm run deploy
```
*(Wrangler will prompt you to log into your Cloudflare account if not already logged in).*

---

## 📤 Pushing to Git

When you are ready to make your first commit and push to your remote repository:

```bash
# 1. Stage all production files
git add .

# 2. Make your initial commit
git commit -m "feat: initial production release of Elan & nVision 2027 sponsorship flipbook"

# 3. Connect your remote repository (replace with your repo URL)
git remote add origin https://github.com/<your-username>/<your-repo-name>.git

# 4. Push to GitHub / GitLab
git branch -M main
git push -u origin main
```

---

## ⌨️ Controls & Shortcuts

| Action | Control |
| :--- | :--- |
| **Next Page** | Click right page edge, click `→` button, or press `ArrowRight` / `Space` |
| **Previous Page** | Click left page edge, click `←` button, or press `ArrowLeft` |
| **Jump to Section** | Select from TOC dropdown in the bottom control dock |
| **Toggle Fullscreen** | Click `⛶` in the top right corner |
| **Export to PDF** | Press `Ctrl + P` (or `Cmd + P`) and select "Save as PDF" |

---

## 👥 Contacts & Credits

- **Festival**: Elan & ηVision 2027, IIT Hyderabad
- **Dates**: January 22–25, 2027
- **Sponsorship Lead**: Shreedhanvi Yadlapally (`sponsorship@elannvision.in` | `+91 83328 73230`)
- **Official Website**: [elannvision.iith.ac.in](https://elannvision.iith.ac.in)
- **Instagram**: [@elan_iith](https://www.instagram.com/elan_iith/) · [@nvision_iith](https://www.instagram.com/nvision_iith/)
