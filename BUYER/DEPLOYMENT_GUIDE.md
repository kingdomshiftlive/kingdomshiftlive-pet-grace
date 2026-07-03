# Cloudflare Pages Deployment Guide

## Prerequisites
- GitHub account (free)
- Cloudflare account (free)
- Node.js 18+ installed locally

## Step 1 — Push to GitHub

```bash
# In the project folder
git init
git add .
git commit -m "Initial deployment"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/my-pet-grace.git
git push -u origin main
```

Create the GitHub repo first at: github.com/new
- Name: `my-pet-grace`
- Visibility: Public
- Do NOT initialize with README

## Step 2 — Connect Cloudflare Pages

1. Go to dash.cloudflare.com
2. Click **Workers & Pages** in the left sidebar
3. Click **Create** → **Pages** → **Connect to Git**
4. Authorize GitHub
5. Select your `my-pet-grace` repository
6. Click **Begin setup**

## Step 3 — Build Settings

| Setting | Value |
|---|---|
| Project name | `my-pet-grace` |
| Production branch | `main` |
| Framework preset | Vite |
| Build command | `npm run build` |
| Build output directory | `dist` |

Click **Save and Deploy**.

Build takes approximately 60 seconds. You receive a free URL:
`https://my-pet-grace.pages.dev`

## Step 4 — Environment Variables

In Cloudflare Pages → your project → **Settings** → **Environment Variables**:

| Variable | Value |
|---|---|
| `VITE_ANTHROPIC_API_KEY` | Your Anthropic API key |

Click **Encrypt** to secure the key. Then go to **Deployments** → **Retry deployment**.

Get your Anthropic key at: console.anthropic.com (pay-as-you-go, ~$0.01/conversation)

## Step 5 — Custom Domain

1. In Cloudflare Pages → your project → **Custom Domains**
2. Click **Set up a custom domain**
3. Enter your domain name
4. If domain is registered with Cloudflare Registrar: automatic
5. If domain is elsewhere: update nameservers to Cloudflare

**Recommended:** Register your domain through Cloudflare Registrar (dash.cloudflare.com → Domain Registration). Cloudflare sells domains at cost with no markup, and DNS is automatic.

SSL certificate provisions automatically. No additional setup.

## Step 6 — Verify Deployment

Check these after deployment:
- [ ] Home page loads
- [ ] Navigation works on all pages
- [ ] Dark/light mode toggles
- [ ] AI Pet Advisor sends and receives messages
- [ ] Contact form submits without errors
- [ ] Blog posts load individually
- [ ] Tools page renders all tools

## Redeployment

After any code change:
```bash
git add .
git commit -m "describe your change"
git push origin main
```

Cloudflare Pages detects the push and redeploys automatically. Live in ~60 seconds.
