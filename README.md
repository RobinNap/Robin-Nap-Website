# Robin Nap - Personal Website

A minimal, elegant personal website with three main sections: Work, Apps, and Music.

## Deploying to Cloudflare Pages via GitHub

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon → **New repository**
3. Name it something like `robinnap-website` or `personal-site`
4. Keep it public or private (your choice)
5. Click **Create repository**

### Step 2: Push Your Code to GitHub

In your terminal, navigate to this project folder and run:

```bash
git init
git add .
git commit -m "Initial commit - personal website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and repository name.

### Step 3: Connect to Cloudflare Pages

1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com)
2. Select **Workers & Pages** from the sidebar
3. Click **Create application** → **Pages** → **Connect to Git**
4. Authorize Cloudflare to access your GitHub account
5. Select the repository you just created
6. Configure your build settings:
   - **Project name:** `robinnap` (or whatever you prefer)
   - **Production branch:** `main`
   - **Build command:** (leave empty - it's a static site)
   - **Build output directory:** (leave empty or use `/`)
7. Click **Save and Deploy**

### Step 4: Connect Your Custom Domain

1. In Cloudflare Pages, go to your project
2. Click **Custom domains** → **Set up a custom domain**
3. Enter `robinnap.com`
4. Follow the prompts to configure DNS (if your domain is already on Cloudflare, it will be automatic)
5. Wait for SSL certificate to provision (usually a few minutes)

Your site will be live at `robinnap.com`!

## Local Development

To preview the site locally, you can use any static server. For example:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js (npx)
npx serve
```

Then open `http://localhost:8000` in your browser.

## Customization

- **Edit content:** Update the HTML files directly (`index.html`, `work.html`, `apps.html`, `music.html`)
- **Change colors:** Modify the CSS variables in `styles.css` under `:root`
- **Add pages:** Create new HTML files following the existing template structure

## File Structure

```
├── index.html      # Main landing page with 3 navigation buttons
├── work.html       # Work/professional experience page
├── apps.html       # Apps/projects page
├── music.html      # Music page
├── styles.css      # All styling
└── README.md       # This file
```

