# Buyer Transfer Checklist

Complete transfer takes approximately 20–30 minutes. The site stays live throughout — zero downtime.

## Pre-Transfer (Seller)
- [ ] Confirm Flippa payment cleared through escrow
- [ ] Export email list CSV if one was built (Mailchimp → Audience → Export)
- [ ] Export Google Analytics access if connected

---

## Step 1 — GitHub Repository Transfer

1. Go to github.com → log in
2. Navigate to the My Pet Grace repository
3. Click **Settings** tab
4. Scroll to bottom → **Danger Zone**
5. Click **Transfer**
6. Type the repository name to confirm
7. Enter buyer's GitHub username
8. Click **I understand, transfer this repository**

Buyer receives email invitation and must accept.

- [ ] Seller initiates transfer
- [ ] Buyer accepts transfer email
- [ ] Buyer confirms repository is visible in their GitHub account

---

## Step 2 — Cloudflare Pages Transfer

1. Log in to dash.cloudflare.com
2. Go to **Workers & Pages** → click My Pet Grace project
3. Go to **Settings** → **General**
4. Scroll to **Transfer project**
5. Enter buyer's Cloudflare account email
6. Click **Transfer**

Buyer receives email and must accept. Site stays live throughout.

- [ ] Seller initiates Cloudflare Pages transfer
- [ ] Buyer accepts transfer in their Cloudflare account
- [ ] Buyer confirms site still loads at pages.dev URL

---

## Step 3 — Custom Domain (if applicable)

If a custom domain was connected:

**If domain is on Cloudflare Registrar:**
1. Cloudflare → Domain Registration → select domain
2. Transfer to buyer's Cloudflare account

**If domain is on another registrar (GoDaddy, Namecheap, etc.):**
1. Unlock the domain at current registrar
2. Request authorization (EPP) code
3. Send code to buyer
4. Buyer initiates transfer at their registrar
5. Transfer takes 5–7 days

- [ ] Domain transfer initiated
- [ ] Buyer confirms domain resolves correctly

---

## Step 4 — Environment Variables

Buyer must create their own API keys — these cannot be transferred (tied to personal accounts and billing):

- [ ] Buyer creates Anthropic account at console.anthropic.com
- [ ] Buyer generates new API key
- [ ] Buyer adds `VITE_ANTHROPIC_API_KEY` to Cloudflare Pages environment variables
- [ ] Buyer redeploys — AI Pet Advisor confirmed working

---

## Step 5 — Affiliate Links

Affiliate accounts are personal — tied to tax ID and payment info. Cannot be transferred.

- [ ] Buyer signs up for affiliate programs (list in README)
- [ ] Buyer updates affiliate URLs in `src/data/siteData.js`
- [ ] Buyer pushes to GitHub — Cloudflare Pages redeploys

---

## Step 6 — Analytics

If Google Analytics was connected:
1. GA4 → Admin → Account Access Management
2. Add buyer's Google account as Administrator
3. Seller removes own access after buyer confirms

- [ ] Buyer added as GA4 administrator
- [ ] Seller removed from GA4

---

## Step 7 — Email List (if applicable)

If a Mailchimp list was built:
1. Mailchimp → Audience → Manage Audience → Export Audience
2. Download CSV
3. Send CSV to buyer
4. Buyer imports into their own Mailchimp account

Per CAN-SPAM and GDPR, subscribers should be notified of ownership change.

- [ ] CSV exported and sent to buyer
- [ ] Buyer imports list
- [ ] Notification sent to subscribers

---

## Transfer Complete Verification

- [ ] Buyer owns GitHub repository
- [ ] Buyer owns Cloudflare Pages project
- [ ] Site loads correctly at custom domain
- [ ] AI Pet Advisor works with buyer's API key
- [ ] Buyer has affiliate account signups underway
- [ ] Escrow released to seller

**Transfer complete.**
