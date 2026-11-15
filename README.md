# leonidalog.app

Static site for the Leonida Log app (repo and domain keep the Sunset State
name): landing page, privacy policy, terms of use, support, and the content
the app reads over the air. Served by GitHub Pages, set up like
`vinewoodvault-site`.

| File | URL | Read by |
|---|---|---|
| `index.html` | `/` | |
| `privacy.html` | `/privacy` | listing, paywall |
| `terms.html` | `/terms` | paywall |
| `support.html` | `/support` | listing |
| `pois.json` | `/pois.json` | `POIStore` (map content, `live` flag) |
| `news.json` | `/news.json` | `NewsFeedModel` announcements |
| `giveaway.json` | `/giveaway.json` | `Giveaway` (ships `"draft": true`) |

## DNS

On the `leonidalog.app` zone (Cloudflare, proxied): apex A/AAAA to GitHub Pages; Workers serve /overlay/*, /go/*, /api/overlay/* and /api/giveaway/*. leonidalog.djr.li (Dan's zone) 301s everything here.
