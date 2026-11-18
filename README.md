# open.scenaristapp.com

A second address for scene links from scenaristapp.com, so the website's
Open in Scenarist buttons can be universal links: a link to the domain a
visitor is already on stays in Safari, and the `scenarist://` scheme shows
an error where the app isn't installed.

- `.well-known/apple-app-site-association` lets Scenarist (1.14 and later,
  `applinks:open.scenaristapp.com`) claim every page here.
- `index.html` and `404.html` send a browser on to
  `https://scenaristapp.com/open/` with the same fragment (`#f=…`, the scene
  as base64url Fountain), which shows the scene read only. The scene never
  reaches a server.
- GitHub Pages from `main`; `CNAME` sets the domain. `.nojekyll` so
  `.well-known/` is published. DNS: `open` CNAME `nikvy.github.io`, DNS only.
