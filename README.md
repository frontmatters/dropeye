# Dropeye — landing site

Static marketing page for [Dropeye](https://github.com/frontmatters) — a macOS
menu-bar app that turns your Mac into a shared clipboard/pinboard for the local
network. Single self-contained `index.html` (inline CSS/JS, web fonts + Lemon.js
loaded from CDN). No build step.

## Preview

```sh
python3 -m http.server 8791   # then open http://localhost:8791
```

Append `?theme=light` or `?theme=dark` to force a theme (the header toggle also
persists a choice in `localStorage`).

## Checkout

The "Buy a license" buttons carry `class="lemonsqueezy-button"`, so with
[Lemon.js](https://docs.lemonsqueezy.com/help/lemonjs) loaded the Lemon Squeezy
checkout opens as an **overlay on this page** instead of redirecting away.

## Before going live — fill the placeholders

- **Price** — currently `€19` (appears 3×). Set the real price.
- **Download link** — the "Download the free trial" button points at `#`. Point it
  at the hosted, notarized `.dmg`.
- **Checkout URL** — already wired to the live product
  (`frontmatters.lemonsqueezy.com/checkout/buy/84151918-…`).

## Deploy

Any static host works (Cloudflare Pages, Netlify, GitHub Pages, Vercel). It's one
file — point the host at this repo's root, no build command.
