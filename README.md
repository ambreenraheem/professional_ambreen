# 🌐 Ambreen Abdul Raheem — Personal Portfolio Website

> A clean, minimal personal portfolio website built with pure **HTML, CSS, and JavaScript**.  
> No frameworks. No backend. No cost. Hosted free on GitHub Pages.

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Live Demo](#live-demo)
- [Pages & Features](#pages--features)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [How to Run Locally](#how-to-run-locally)
- [How to Deploy on GitHub Pages](#how-to-deploy-on-github-pages)
- [How to Customize](#how-to-customize)
- [Setting Up the Contact Form](#setting-up-the-contact-form)
- [Author](#author)

---

## 📌 About the Project

This is my personal portfolio website — designed to present my work, skills, certificates,
and writing in a professional, fast-loading, and mobile-friendly format.

**Why not Streamlit?**  
My previous portfolio used Streamlit (a Python framework for data apps). While it worked,
Streamlit has limitations for portfolio sites: cold-start loading delays, a visible
"built with Streamlit" branding, and no custom domain support on the free plan.

This HTML version solves all of that:

- ✅ Loads instantly (static files, no server needed)
- ✅ Works on any device — mobile, tablet, desktop
- ✅ Completely free hosting on GitHub Pages — forever
- ✅ No sleeping, no spinners, no third-party branding
- ✅ Easy to update — just edit the HTML file

---

## 🔗 Live Demo

```
https://YOUR-USERNAME.github.io
```

> Replace `YOUR-USERNAME` with your actual GitHub username after deployment.

---

## 📄 Pages & Features

The entire site is a **Single Page Application (SPA)** — meaning all 6 pages live
inside one `index.html` file. JavaScript switches between them by showing/hiding
sections. No page reloads happen.

| Page | What's on it |
|------|-------------|
| 🏠 **Home** | Hero banner with name & title, tech stack chips, 3 featured project cards, contact CTA |
| 👩‍💻 **About** | Bio paragraph, 4 stat cards, skill progress bars, learning timeline |
| 📂 **Projects** | 4 detailed project cards with tech tags, descriptions, and live demo links |
| 🏆 **Certificates** | 6 certificate cards with issuer, year, skill tags, and view links |
| ✍️ **Blog** | 6 blog post cards with category, reading time, excerpt, and read-more links |
| 📬 **Contact** | Contact info column + a working contact form (powered by Formspree) |

### ✨ UI/UX Features

- **Fixed navigation bar** with frosted glass effect — stays visible while scrolling
- **Mobile hamburger menu** — full dropdown navigation on small screens
- **Scroll-triggered animations** — every section fades up smoothly as you scroll
- **Animated skill progress bars** — fill from 0% to target value on scroll
- **Hover effects** on all cards — lift, shadow, and accent bar animation
- **Responsive layout** — works on screens from 320px (small phone) to 1440px+ (desktop)
- **Dot grid background texture** in hero and CTA sections for visual depth
- **Teal accent color** applied consistently as a brand color throughout

---

## 🗂️ Project Structure

```
your-portfolio/
│
├── index.html          ← The ENTIRE website lives in this one file
│
├── README.md           ← This file — project documentation
│
└── assets/             ← (Optional) Create this folder for your photos
    └── profile.jpg     ← Your profile photo (add this yourself)
```

### Why only one file?

For a static portfolio, a single `index.html` is the simplest and most reliable
approach for GitHub Pages. There is nothing to install, no build step, no
configuration — you upload one file and the site works.

### Inside `index.html`

The file is organized into four clear sections:

```
index.html
│
├── <head>
│   ├── Meta tags (SEO, viewport)
│   ├── Google Fonts link (Cormorant Garamond + Outfit)
│   └── <style> block — ALL CSS is written here
│       ├── CSS Variables (colors, fonts, spacing)
│       ├── Reset styles
│       ├── Animation keyframes
│       ├── Navigation styles
│       ├── Shared/reusable component styles
│       ├── Page-specific styles (Hero, About, Projects, etc.)
│       └── Responsive breakpoints (@media queries)
│
└── <body>
    ├── <nav> — Fixed top navigation bar
    ├── <div class="mobile-menu"> — Mobile dropdown
    │
    ├── <div id="page-home">     — Home page content
    ├── <div id="page-about">    — About page content
    ├── <div id="page-projects"> — Projects page content
    ├── <div id="page-certificates"> — Certificates page
    ├── <div id="page-blog">     — Blog page content
    └── <div id="page-contact">  — Contact page content
    │
    └── <script> — ALL JavaScript is written here
        ├── showPage()       — switches between pages
        ├── toggleMenu()     — opens/closes mobile menu
        ├── initReveal()     — scroll-triggered animations
        ├── initSkillBars()  — animates progress bars
        └── Contact form handler (Formspree AJAX submission)
```

---

## 🛠️ Technologies Used

| Technology | Purpose | Why chosen |
|------------|---------|------------|
| **HTML5** | Page structure and content | Universal, no setup needed |
| **CSS3** | Styling, layout, animations | Full control, no library needed |
| **JavaScript (Vanilla)** | Page switching, animations, form | No framework overhead |
| **CSS Grid & Flexbox** | Responsive layouts | Modern, widely supported |
| **CSS Variables** | Consistent design tokens (colors, fonts) | Easy to retheme |
| **IntersectionObserver API** | Scroll-triggered animations | Efficient, no scroll listeners |
| **Google Fonts** | Cormorant Garamond + Outfit | Distinctive typography |
| **Formspree** | Contact form backend | Free, no server code needed |
| **GitHub Pages** | Hosting | Free, fast, reliable |

---

## 💻 How to Run Locally

Running this project on your own computer requires **no installation at all** —
you just need a web browser and one of the methods below.

---

### Method 1: Open directly (Simplest)

1. Download or clone this repository
2. Find the `index.html` file in your folder
3. Double-click `index.html`
4. It opens in your default browser

> ⚠️ **Note:** This method works for viewing but the contact form won't work
> locally (Formspree requires a live URL). Everything else works perfectly.

---

### Method 2: Using VS Code Live Server (Recommended)

This method gives you live reloading — the browser refreshes automatically
every time you save a change to the file.

**Step 1 — Install VS Code**
```
Download from: https://code.visualstudio.com
```

**Step 2 — Install the Live Server extension**
```
1. Open VS Code
2. Press Ctrl + Shift + X  (opens Extensions panel)
3. Search: Live Server
4. Click Install on the extension by Ritwick Dey
```

**Step 3 — Open your project**
```
1. In VS Code: File → Open Folder
2. Select the folder containing index.html
```

**Step 4 — Start the server**
```
Option A: Right-click index.html in the sidebar → "Open with Live Server"
Option B: Click "Go Live" button in the bottom-right status bar
```

**Step 5 — View in browser**
```
Browser opens automatically at: http://127.0.0.1:5500
```

Now every time you save `index.html`, the browser refreshes instantly. ✅

---

### Method 3: Using Python (if you have Python installed)

**Step 1 — Open Terminal / Command Prompt**
```
Windows: Press Win + R, type "cmd", press Enter
Mac/Linux: Open Terminal app
```

**Step 2 — Navigate to your project folder**
```bash
cd path/to/your/portfolio
# Example on Windows: cd C:\Users\Ambreen\Desktop\portfolio
# Example on Mac:     cd /Users/ambreen/Desktop/portfolio
```

**Step 3 — Start a local server**
```bash
# Python 3 (most computers):
python -m http.server 8000

# Python 2 (older computers):
python -m SimpleHTTPServer 8000
```

**Step 4 — Open in browser**
```
Go to: http://localhost:8000
```

**Step 5 — Stop the server**
```
Press Ctrl + C in the terminal
```

---

## 🚀 How to Deploy on GitHub Pages

GitHub Pages hosts static websites for **free, forever**, with no sleeping
and no usage limits. Here is the complete step-by-step process:

---

### Step 1 — Create a GitHub Account

If you don't have one:
```
Go to: https://github.com
Click: Sign up
```

---

### Step 2 — Create the Repository

> ⚠️ **The repository name is very important.** It must follow this exact format:

```
YOUR-GITHUB-USERNAME.github.io
```

Example: if your GitHub username is `ambreen-dev`, the repo name must be:
```
ambreen-dev.github.io
```

**How to create it:**
```
1. Go to https://github.com/new
2. Repository name: YOUR-USERNAME.github.io
3. Set to: Public  ← must be Public for free GitHub Pages
4. Check: Add a README file  ← optional, you already have one
5. Click: Create repository
```

---

### Step 3 — Upload Your Files

**Option A: Upload via Browser (No Git required — easiest)**

```
1. Open your new repository on GitHub
2. Click "Add file" → "Upload files"
3. Drag and drop your index.html file (and README.md)
4. Scroll down, write a commit message: "Initial portfolio upload"
5. Click "Commit changes"
```

**Option B: Using Git (recommended for future updates)**

```bash
# Step 1: Initialize Git in your project folder
git init

# Step 2: Add all files to staging
git add .

# Step 3: Create your first commit
git commit -m "Initial portfolio upload"

# Step 4: Connect to your GitHub repository
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git

# Step 5: Push to GitHub
git push -u origin main
```

---

### Step 4 — Enable GitHub Pages

```
1. Go to your repository on GitHub
2. Click the "Settings" tab (top menu)
3. In the left sidebar, click "Pages"
4. Under "Source", select: Deploy from a branch
5. Under "Branch", select: main
6. Under "Folder", select: / (root)
7. Click "Save"
```

---

### Step 5 — Wait & Visit

```
Wait 1–3 minutes for GitHub to build your site.

Then visit: https://YOUR-USERNAME.github.io
```

> 💡 GitHub sends you an email when the site is ready.
> You can also check the "Actions" tab in your repo to see the build progress.

---

### How to Update Your Site After Changes

Every time you want to update the site, just upload the new `index.html`:

**Via Browser:**
```
1. Go to your repo → index.html → click the pencil icon (Edit)
2. Paste your new code
3. Click "Commit changes"
4. Site updates in ~1 minute
```

**Via Git:**
```bash
git add index.html
git commit -m "Update: added new project card"
git push
```

---

## 🎨 How to Customize

All changes are made inside `index.html`. Open it in VS Code (or any text editor)
and find the section you want to change.

### Change your name
```html
<!-- Search for: Ambreen Abdul Raheem -->
<!-- Replace with your name everywhere it appears -->
```

### Change the accent color
```css
/* Find this line in the <style> section: */
--accent: #2a6f8e;

/* Replace with any color you like. Examples: */
--accent: #e63946;   /* red */
--accent: #2d6a4f;   /* forest green */
--accent: #7b2d8b;   /* purple */
--accent: #e76f51;   /* orange */
```

### Add your profile photo
```html
<!-- Find this inside the About page section: -->
<span class="about-placeholder">🧑‍💻</span>

<!-- Replace with: -->
<img src="assets/profile.jpg" alt="Your Name" />

<!-- Then create an 'assets' folder and put your photo inside it -->
```

### Add a new project card
```html
<!-- Copy this block and fill in your details: -->
<div class="project-card js-reveal">
  <div class="project-icon">🔧</div>
  <div class="project-tags">
    <span class="tag">Python</span>
    <span class="tag">Streamlit</span>
  </div>
  <h3 class="project-title">Your Project Name</h3>
  <p class="project-desc">
    Describe what the project does, what problem it solves,
    and what technologies you used.
  </p>
  <div class="project-footer">
    <a class="project-link" href="YOUR-LIVE-LINK" target="_blank">Live Demo →</a>
  </div>
</div>
```

### Add a new certificate
```html
<!-- Copy this block: -->
<div class="cert-card js-reveal">
  <div class="cert-badge">🏆</div>
  <div class="cert-issuer">Platform Name (e.g. Coursera)</div>
  <div class="cert-title">Certificate Title Here</div>
  <div class="cert-date">📅 2025</div>
  <div class="cert-skills">
    <span class="cert-skill-tag">Skill 1</span>
    <span class="cert-skill-tag">Skill 2</span>
  </div>
  <a class="cert-link" href="YOUR-CERTIFICATE-URL" target="_blank">View Certificate →</a>
</div>
```

---

## 📬 Setting Up the Contact Form

The contact form uses **Formspree** — a free service that receives form submissions
and forwards them to your email. No backend code needed.

### Step 1 — Create a Formspree account
```
Go to: https://formspree.io
Click: Get Started (free)
Sign up with your email
```

### Step 2 — Create a new form
```
1. Click "+ New Form"
2. Give it a name: "Portfolio Contact"
3. Set your email address for receiving messages
4. Formspree gives you a URL like: https://formspree.io/f/xabc1234
```

### Step 3 — Update index.html
```html
<!-- Find this line in the Contact page section: -->
<form id="contactForm" action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST">

<!-- Replace YOUR_FORMSPREE_ID with your actual ID, e.g.: -->
<form id="contactForm" action="https://formspree.io/f/xabc1234" method="POST">
```

### Step 4 — Update the redirect URL
```html
<!-- Find this hidden input in the form: -->
<input type="hidden" name="_next" value="https://YOUR-SITE-URL" />

<!-- Replace with your actual GitHub Pages URL: -->
<input type="hidden" name="_next" value="https://your-username.github.io" />
```

### Step 5 — Test it
```
1. Deploy your site
2. Fill in the contact form and submit
3. Check your email — you should receive the message within seconds
```

> 💡 Free Formspree allows **50 submissions per month** — more than enough
> for a personal portfolio.

---

## 👩‍💻 Author

**Ambreen Abdul Raheem**  
Data Analyst & Web App Developer  
📍 Karachi, Pakistan

- 🌐 Portfolio: [your-username.github.io](https://your-username.github.io)
- 💼 LinkedIn: [linkedin.com/in/YOUR-USERNAME](https://linkedin.com/in/YOUR-USERNAME)
- 🐙 GitHub: [github.com/YOUR-USERNAME](https://github.com/YOUR-USERNAME)
- 📧 Email: your@email.com

---

## 📝 License

This project is open source. Feel free to use it as a template for your own
portfolio — just replace the content with your own information.

---

*Built with ❤️ in Karachi — pure HTML, CSS, and JavaScript, no frameworks needed.*
