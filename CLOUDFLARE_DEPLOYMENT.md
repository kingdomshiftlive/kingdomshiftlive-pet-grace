# Cloudflare Pages Deployment Guide — My Pet Grace

## Overview

My Pet Grace is built for Cloudflare Pages — free hosting, automatic SSL, global CDN, and automatic deploys on every GitHub push.

---

## Step 1 — Connect GitHub to Cloudflare Pages

1. Go to **dash.cloudflare.com**
2. Click **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
3. Authorize GitHub when prompted
4. Select your `my-pet-grace` repository
5. Click **Begin setup**

---

## Step 2 — Build Configuration

| Setting | Value |
|---|---|
| Project name | `my-pet-grace` |
| Production branch | `main` |
| Framework preset | Vite |
| Build command | `npm run build` |
| Build output directory | `dist` |

Click **Save and Deploy**. First build takes ~90 seconds.

---

## Step 3 — Environment Variables

Go to your project → **Settings** → **Environment Variables** → **Production**

| Variable Name | Value | Notes |
|---|---|---|
| `VITE_ANTHROPIC_API_KEY` | `sk-ant-...` | Get at console.anthropic.com |

Click **Encrypt** on the key value. Then trigger a new deployment:
Deployments → latest deployment → **Retry deployment**

---

## Step 4 — Connect Custom Domain

**Option A — Domain registered with Cloudflare (recommended):**
1. Pages → your project → **Custom Domains** → **Set up a custom domain**
2. Enter your domain
3. DNS configures automatically
4. SSL provisions automatically (usually under 60 seconds)

**Option B — Domain at another registrar:**
1. Pages → Custom Domains → Set up a custom domain
2. Enter your domain
3. Cloudflare shows you DNS records to add
4. Log in to your registrar and add those records
   - Or update nameservers to Cloudflare for full DNS control
5. SSL provisions once DNS propagates (up to 24 hours)

---

## Step 5 — Verify Everything Works

After deployment, check:

- [ ] Site loads at your domain
- [ ] HTTPS padlock appears (SSL active)
- [ ] All 12 pages load without errors
- [ ] Dark/light mode toggle works
- [ ] AI Pet Advisor sends and receives responses
- [ ] Contact form submits successfully
- [ ] Blog posts open individually

---

## Redeployment (After Any Code Change)

```bash
git add .
git commit -m "your change description"
git push origin main
```

Cloudflare Pages detects the push and redeploys automatically. Live in ~60 seconds.

---

## Rollback

If a deployment breaks something:
1. Pages → your project → **Deployments**
2. Find the last working deployment
3. Click the three-dot menu → **Rollback to this deployment**

Instant rollback with zero downtime.

---

## Cloudflare Registrar (Recommended for New Domains)

Cloudflare sells domains at wholesale cost — no markup. Compared to GoDaddy or Namecheap, you typically save $5–$15/year per domain.

Register at: **dash.cloudflare.com → Domain Registration**

Domains registered here are automatically on Cloudflare DNS. Connect to Pages in one click.
