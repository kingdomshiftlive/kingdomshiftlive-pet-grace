# Buyer Transfer Guide — My Pet Grace

This document walks seller and buyer through the complete transfer process. The site stays live throughout — zero downtime.

---

## Before Transfer

**Seller confirms:**
- [ ] Flippa escrow payment received and cleared
- [ ] All site functionality working (do a final check)
- [ ] Email list exported if one was built

**Buyer prepares:**
- [ ] GitHub account ready (github.com — free)
- [ ] Cloudflare account ready (cloudflare.com — free)
- [ ] Anthropic account ready (console.anthropic.com — free, pay per use)

---

## Transfer 1 — GitHub Repository

**Seller steps:**
1. github.com → log in → navigate to the My Pet Grace repository
2. **Settings** → scroll to **Danger Zone** → **Transfer**
3. Type the repository name to confirm
4. Enter buyer's GitHub username → **I understand, transfer this repository**

**Buyer steps:**
1. Accept the transfer invitation email from GitHub
2. Confirm the repository is visible in your GitHub account

✓ Complete when buyer can see the repository at `github.com/BUYER_USERNAME/my-pet-grace`

---

## Transfer 2 — Cloudflare Pages Project

**Seller steps:**
1. dash.cloudflare.com → Workers & Pages → click My Pet Grace
2. **Settings** → **General** → scroll to **Transfer project**
3. Enter buyer's Cloudflare account email → **Transfer**

**Buyer steps:**
1. Accept the transfer email in your Cloudflare account
2. Confirm site still loads at `.pages.dev` URL

✓ Complete when buyer sees the project in their Cloudflare dashboard

---

## Transfer 3 — Custom Domain (if applicable)

**If domain is on Cloudflare Registrar:**
- Seller: Domain Registration → select domain → Transfer to another account → enter buyer email

**If domain is on another registrar:**
- Seller: unlock domain, get EPP/authorization code, send to buyer
- Buyer: initiate transfer at their registrar using the code
- Allow 5–7 days for completion

✓ Complete when domain resolves to buyer's Cloudflare Pages project

---

## Transfer 4 — Environment Variables

The AI Pet Advisor API key cannot be transferred — it's tied to the seller's Anthropic billing account.

**Buyer steps:**
1. Create account at console.anthropic.com
2. API Keys → Create Key → copy the key
3. Cloudflare Pages → your project → Settings → Environment Variables
4. Add `VITE_ANTHROPIC_API_KEY` with your new key, click Encrypt
5. Deployments → Retry deployment
6. Test the AI Pet Advisor — confirm it responds

✓ Complete when AI Pet Advisor works with buyer's key

---

## Transfer 5 — Affiliate Links

Affiliate accounts are personal (tied to tax ID and payment info) and cannot be transferred. This is standard for all website sales.

**Buyer steps:**
1. Sign up for affiliate programs listed in the README
2. Open `src/data/siteData.js`
3. Replace affiliate URLs with your own affiliate links
4. `git push origin main` → Cloudflare deploys automatically

Priority programs to sign up for first:
- Chewy: chewy.com/affiliates
- 1800PetMeds: 1800petmeds.com/affiliates
- BarkBox: barkbox.com/affiliates
- HolistaPet: holistapet.com/affiliates

✓ Complete when your affiliate links are live on the site

---

## Transfer 6 — Analytics (if connected)

**If Google Analytics was set up:**
1. GA4 → Admin → Account Access Management
2. Seller adds buyer's Google account as Administrator
3. Seller removes their own access after buyer confirms

✓ Complete when buyer has sole admin access to GA4 property

---

## Transfer 7 — Email List (if built)

**If Mailchimp list exists:**
1. Mailchimp → Audience → Manage Audience → Export Audience → download CSV
2. Seller sends CSV to buyer
3. Buyer imports into their own Mailchimp account
4. Per CAN-SPAM/GDPR: notify subscribers of ownership change

✓ Complete when buyer has imported list and sent ownership notification

---

## Final Verification

- [ ] Buyer owns GitHub repository
- [ ] Buyer owns Cloudflare Pages project
- [ ] Site loads at custom domain with SSL
- [ ] AI Pet Advisor works with buyer's API key
- [ ] Affiliate links updated with buyer's URLs
- [ ] Analytics access transferred
- [ ] Email list transferred (if applicable)
- [ ] Flippa escrow released to seller

**Transfer complete. Good luck with My Pet Grace.**
