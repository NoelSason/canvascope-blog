# Canvascope Newsroom (redirect shim)

This site was **merged into the main Canvascope site**. The newsroom now lives at:

**https://www.canvascope.org/newsroom**

`blog.canvascope.org` now serves only `vercel.json`, which 301-redirects every path
to the main domain (catch-all → `/newsroom`; `llms.txt`, `canvascope.md`,
`sitemap.xml`, `robots.txt` → their `www.canvascope.org` equivalents).

The old static files (`index.html`, `canvascope-blog.html`, `canvascope.md`,
`llms.txt`, `sitemap.xml`, `robots.txt`) are kept for history but are no longer
served, since redirects take precedence over the filesystem. To restore the
standalone blog, revert the `vercel.json` change.
