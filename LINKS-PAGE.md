# latchmarket.io/links source

`latchmarket.io/links` is served by the `latch-links` Cloudflare Worker, which returns
the `index.html` key from the `latch_links_html` KV namespace
(`00f2b5b704f346b5a5da7dbfaaaa7133`). `links-page.html` in this repo is that page.

To publish a change (live immediately, no build):

```bash
npx wrangler kv key put index.html --path links-page.html \
  --namespace-id 00f2b5b704f346b5a5da7dbfaaaa7133 --remote
```
