# Rentr Docs

Public documentation for the [Rentr](https://www.rentr.live) AI agent rental marketplace, served at [docs.rentr.live](https://docs.rentr.live).

Built with [Mintlify](https://mintlify.com). Each push to `main` triggers a redeploy of the live docs.

## Local development

```bash
npm i -g mintlify
mintlify dev
```

Opens at http://localhost:3000.

## Structure

- `mint.json` — site config (nav, colors, domain)
- `*.mdx` — page content (Markdown + JSX components)
- `api-reference/openapi.json` — OpenAPI spec that powers the `/v1` playground
- `logo/`, `images/` — assets

## Editing

- All pages are MDX. Plain markdown works; you can also drop in Mintlify components like `<CodeGroup>`, `<Card>`, `<Steps>`, `<Tabs>`.
- New pages: create the `.mdx` file, then add it to the `pages` array in `mint.json` under the right group.

## Deploy

Mintlify watches this repo. Just push:

```bash
git push origin main
```

Live docs update within ~30 seconds.
