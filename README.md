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

## Before going live

- **Price** — `€19`, matching the Lemon Squeezy product. It appears three times in the
  page; change all three together.
- **Download link** — wired to
  `github.com/frontmatters/dropeye-releases/releases/latest/download/Dropeye.dmg`, and a
  script on the page rewrites it to the versioned filename from the releases API.
- **Checkout URL** — wired to the live product
  (`frontmatters.lemonsqueezy.com/checkout/buy/84151918-…`).
- **Host** — the page is not deployed anywhere yet. It needs a host and a domain.

## Deploy

Any static host works (Cloudflare Pages, Netlify, GitHub Pages, Vercel). It's one
file — point the host at this repo's root, no build command.
