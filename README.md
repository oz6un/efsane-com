# efsane.com — domain sale landing page

A single static page (`index.html`, no dependencies, no build step) advertising
efsane.com for sale. Offers route to `hbilis@efsane.com.tr`.

Turkish by default, with an EN toggle in the top right; the choice is remembered
in `localStorage`. Copy for both languages lives in the `COPY` object at the
bottom of `index.html` — the mailto subject and body are translated too. The two
taglines are deliberately not translations of each other: the English one leans
on "efsane" meaning *legend*, which is not a selling point in Turkish.

Published with GitHub Pages from `main` at the repo root:
https://oz6un.github.io/efsane-com/

## Serving it at efsane.com

The page belongs on the domain being sold. Two steps:

1. **DNS** — at whoever hosts efsane.com's nameservers, point the apex at
   GitHub Pages with four `A` records:

   ```
   @  A  185.199.108.153
   @  A  185.199.109.153
   @  A  185.199.110.153
   @  A  185.199.111.153
   ```

   For `www`, add `www CNAME oz6un.github.io.`

2. **Tell Pages the domain** — add a `CNAME` file to this repo containing
   `efsane.com`, or set it under Settings → Pages → Custom domain. Once DNS
   resolves, enable "Enforce HTTPS" there.

Note that changing efsane.com's DNS replaces whatever it currently points at.

## Editing

Edit `index.html` and push to `main`; Pages redeploys automatically. The price
is deliberately absent — the call to action is "Make an offer".
