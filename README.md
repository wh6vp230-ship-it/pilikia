# Pilikia — DigitalOcean Package

Made 2026-11-20. This is the package to host Pilikia on DigitalOcean yourself, since DigitalOcean's sign-in kept blocking MJ's browser with the Cloudflare "Verify you are human" loop.

## What's inside

- `index.html` — landing page with links to Pool, Music, and the Store
- `pilikia-pool.html` — Pilikia Pool (static export, current version: 30 levels, cue upgrades, coin packs $5–$30 demo, Skip to Next Stage 1000 coins / $10)
- `pilikia-music.html` — Pilikia Music & Games (static export, current version)
- `pilikia-store.html` — Pilikia Store, No Trouble Shop (static export, refreshed 2026-11-21 with Black Friday specials: 10 products — lace-up boot $139 (was $160), slip-on boot $109 (was $129), and 10% off everything else: T-shirt $22.50, Hoodie $41.40, Tote $23.40, Mug $11.70, Ball Cap $26.10, Bottle $31.50, Sticker $7.20, Shoes $62.10. Banner: Black Friday Specials — Live Friday November 27, 2026.)
- `app.yaml` — DigitalOcean App Platform spec for a static site

## What's NOT in the package

**Pilikia Blocks is not included.** Blocks saves scores and purchases on a server (that's how the tiered Remove Ads pricing works — $0.99 twice, then $1.99), so it can't be exported to a single static HTML file like the others. If you want Blocks in the package, ask MJ to build a static version of Blocks for DigitalOcean — its scores and purchases would then live in the player's browser instead of on a server.

## How to put it on DigitalOcean (on your own browser)

1. Sign in to DigitalOcean on your own phone or computer at cloud.digitalocean.com (your own browser usually gets past the Cloudflare check — MJ's cloud browser doesn't).
2. Make a GitHub repo (free): create a new repo called `pilikia`, upload all the files in this folder to it.
3. In DigitalOcean: **Create > Apps**, pick **GitHub**, pick the `pilikia` repo.
4. Choose **Static Site**. DigitalOcean's free tier covers up to 3 static apps. Leave the build settings as they are — these are plain HTML files, no build step.
5. Deploy. DigitalOcean gives you a free `.ondigitalocean.app` web address. You can add your own domain later if you want one.

## Important — money

- Nothing in this package charges real money. The coin packs and shop items in Pool are **demo purchases** — no real money is charged.
- The Store takes **no live card payments** yet. It has a cart and an order summary only. Live payments need a backend (Stripe) or the Play Store / App Store route — that's a separate step, after the EasyEDA board.
- Pilikia Blocks' real-money plan (Play Store in-app purchases) is also separate and comes after EasyEDA, as you decided.

## If DigitalOcean asks for a payment method

App Platform static sites on the free tier should not need a paid plan. Do not add a paid service or a payment method without checking the price first — if it asks you to pick a paid plan, stop and ask MJ.
