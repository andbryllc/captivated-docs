# Captivated Help Center (Mintlify)

This repository contains the Captivated Help Center, migrated from WordPress
(`learn.captivated.works`) to [Mintlify](https://mintlify.com).

## Structure

- `docs.json` — site configuration: theme, brand colors, navigation, navbar, footer.
- `index.mdx` — Help Center home page.
- `getting-started/`, `features/`, `premium-features/`, `administration/`, `faq/`,
  `integrations/`, `updates/` — the help articles as `.mdx` files.
- `logo/` — placeholder brand logos (`logo-light.svg`, `logo-dark.svg`).
- `favicon.svg` — placeholder favicon.

## Preview locally

```bash
npm i -g mint      # install the Mintlify CLI
mint dev           # serve at http://localhost:3000
mint broken-links  # check for broken internal links
```

## Deploy

1. Push this folder to a GitHub repository.
2. In the [Mintlify dashboard](https://dashboard.mintlify.com), connect the repo.
3. Point your `learn.captivated.works` domain at Mintlify (Settings → Custom domain).

## Notes for the team

- **Images** currently load from the existing WordPress media library
  (`https://learn.captivated.works/wp-content/...`). They render immediately. When you
  fully retire WordPress, re-host these images in `/images` and update the URLs.
- **Branding** uses the new blue palette (primary `#009CDB`). Replace the placeholder
  logos in `/logo` and `favicon.svg` with the finalized layered-message-cloud logo when
  it's ready — no other changes needed.
- **Cross-links** between articles still point to the old `learn.captivated.works/help/...`
  URLs. Once the Mintlify site is live at the same domain, these can be rewritten to
  relative paths (e.g. `/features/sending-a-message`).
