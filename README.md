# Shreevidya Akhandmahayog — mobile app

This is a mobile web app (a "PWA") built from the content on shreevidyamahayog.org.
Opened on a phone, it looks and behaves like a native app — its own icon,
no browser address bar, works offline once loaded.

## Files
- `index.html` — the app itself
- `manifest.json` — tells the phone how to install it (name, icon, colors)
- `sw.js` — service worker, caches pages so it still opens with no signal

## Try it right now
Just open `index.html` in a phone browser. The install prompt (Add to Home
Screen) only appears once these files are served from a real web address
(not opened as a local file), so for that step you need to host them.

## Get "Add to Home Screen" working (free, ~5 minutes)
Any static host works. The easiest is **GitHub Pages**:

1. Create a new GitHub repository.
2. Upload `index.html`, `manifest.json`, and `sw.js` to it.
3. In the repo, go to Settings → Pages → set the source to the main branch.
4. GitHub gives you a URL like `https://yourname.github.io/reponame/`.
5. Open that URL on a phone:
   - **Android (Chrome):** menu (⋮) → "Add to Home screen" / "Install app"
   - **iPhone (Safari):** Share icon → "Add to Home Screen"

Other free options that work the same way: Netlify, Vercel, Cloudflare
Pages, or your own web hosting if shreevidyamahayog.org already has one —
in that case this could live at `shreevidyamahayog.org/app/`.

## If you want a real App Store / Play Store listing
That needs a developer account on each store and native packaging. The
standard route is wrapping this same code with a tool like Capacitor —
happy to prepare that build if you want to take it that far.

## Keeping content current
Right now the content (books, events, articles) is hand-copied from the
live site as of today. It won't update itself. Options if that matters:
- Simplest: come back here periodically and ask for a refresh.
- More involved: connect the app to the site's WordPress feed so new
  posts show up automatically — possible, but a bigger build.
