# anton-babaskin.github.io

Redirect stub for [ant0n.dev](https://ant0n.dev/).

This address previously served a second, standalone landing page. It carried
almost the same title, description and project list as ant0n.dev while
declaring itself canonical, so the two competed for the same searches and
split the signals between them.

The page now consolidates into ant0n.dev instead:

- `rel="canonical"` points at `https://ant0n.dev/`, so search engines credit
  the primary site.
- A zero-second meta refresh sends visitors there, with a visible link as a
  fallback. GitHub Pages user sites cannot issue a real 301 without a custom
  domain, so this is the closest equivalent.
- No `noindex`. It would drop this URL without passing anything on; the
  canonical has to stay crawlable to consolidate.

## Files

- `index.html` — the redirect stub.
- `google9c97419bafed66e0.html` — Google Search Console verification file;
  keep it unchanged, it keeps this property visible while the move settles.

`sitemap.xml` was removed. It listed this page for crawling, which is the
opposite of what a redirect stub wants.

## Deployment

GitHub Pages publishes `main` automatically. No build step or dependencies.
