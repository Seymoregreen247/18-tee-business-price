# Click & Print 24-7 — Custom Apparel Portal

**Owner:** Seymore Green — Click & Print 24-7  
**Address:** 35 Poplar St, Roslindale, MA 02131  
**Phone:** 844-4-SEYMOR (844-473-9667)  
**Live URL:** *(set after Netlify deploy)*

---

## What This Is

A fully self-contained custom apparel ordering portal. Customers fill out a lead gate form, browse the product catalog, and place orders directly. Works on desktop and mobile, installs as a PWA (Add to Home Screen), and works offline.

---

## Files In This Repo

| File | Purpose |
|------|---------|
| `index.html` | The entire app — all JS, CSS, and images embedded |
| `manifest.json` | PWA install config (name, icons, theme color) |
| `sw.js` | Service worker — enables offline mode + caching |
| `icon-192.png` | PWA icon (small) |
| `icon-512.png` | PWA icon (large) |
| `netlify.toml` | Netlify build + header/redirect rules |
| `README.md` | This file |

---

## Pre-Launch Checklist (Do Before Pushing)

1. **Formspree** — Go to [formspree.io](https://formspree.io), create a free account, make a new form, copy your Form ID. In `index.html`, search for `YOUR_FORM_ID` and replace it. This makes every order submission email you automatically.

2. **Admin Password** — In `index.html`, search for `CP247admin` (or whatever the current passwords are) and change them to something only you know. Never commit your real passwords to a public repo — use a private repo or change them first.

3. **Custom Domain** — After deploying to Netlify, go to Site Settings → Domain Management and add your domain (e.g. `clickandprint247.com`).

---

## Deploy to Netlify (3 Steps)

1. Push all files in this folder to a GitHub repo under **Seymoregreen247**
2. Go to [netlify.com](https://netlify.com) → Add new site → Import from GitHub → select the repo
3. Netlify auto-deploys. Every time you push a change to GitHub, the site updates automatically.

---

## Pricing Reference

| Garment | Full Color DTF | One Color |
|---------|---------------|-----------|
| T-Shirt (Gildan G500) | $22 | $16 |
| Hoodie (Gildan G18500) | $32 | $24 |
| Crewneck (Gildan G18000) | $28 | $20 |
| Long Sleeve (Gildan G2400) | $24 | $18 |
| Youth Tee (Gildan G500B) | $18 | $13 |
| Hat (Richardson 112) | $25 | $18 |

**Volume Discounts:** 6pc ($0 off) · 12pc ($2 off) · 24pc ($4 off) · 48pc ($6 off) · 100+ ($8 off)

---

## Admin Dashboard

- Click the **Admin** button (top right, badge shows new orders)
- Password protected — your credentials only
- Shows all orders, estimated revenue, leads captured
- Cycle order status: New → Proof Sent → Paid → Fulfilled
- Export all orders to CSV

---

## Payment Methods Accepted

Venmo · PayPal · Cash · Zelle — customers pay after approving their design proof.

---

## Tech Stack

- Pure HTML/CSS/JS — no frameworks, no build step
- All images embedded as base64 (no CDN needed)
- LocalStorage for orders + leads (device-local — see note below)
- Formspree for email notifications on order submit
- PWA-ready (offline, installable on any device)

> **Note:** Orders and leads are stored in the **customer's browser** (localStorage). They are NOT on your device until Formspree emails them to you. Keep Formspree active so you never miss an order.

---

*Built with Claude AI · Seymore Green · Roslindale, Boston*
