# Google Search Console setup (internitylabs.com)

## 1) Add the property

Recommended: **Domain property** (covers http/https + www/non-www)

1. Go to Google Search Console.
2. Click **Add property** → **Domain**.
3. Enter: `internitylabs.com`
4. Google will show you a **DNS TXT record** to add.
5. Add that TXT record in your DNS provider for `internitylabs.com`.
6. Wait for DNS to propagate (usually minutes; sometimes a few hours), then click **Verify**.

Alternative (easier if DNS access is painful): **URL prefix property**

- Add: `https://www.internitylabs.com/`
- Verification methods typically include HTML file upload, meta tag, or GA.

## 2) Submit the sitemap

1. In Search Console, open your property.
2. Left menu → **Sitemaps**.
3. Submit: `sitemap.xml`

Note: the **Sitemaps** screen expects an XML sitemap. If you submit `robots.txt` (or a typo like `robots.tx`), Search Console will show an error like “Your Sitemap does not appear to be in a supported format” because that URL is not an XML sitemap.

Your site already ships these files:
- `https://www.internitylabs.com/sitemap.xml`
- `https://www.internitylabs.com/robots.txt`

## 3) Request indexing for key pages

1. Search Console → **URL inspection**.
2. Paste each URL and click **Request indexing**:
   - `https://www.internitylabs.com/`
   - `https://www.internitylabs.com/products.html`
   - `https://www.internitylabs.com/contact.html`
   - `https://www.internitylabs.com/privacy.html`

## 4) What to monitor (first 1–2 weeks)

- **Pages** (Indexing): make sure important pages are **Indexed**.
- **Sitemaps**: should show **Success** and discovered URLs.
- **Enhancements**: watch for structured-data warnings (if any).
- **Performance**: after data arrives, check queries/countries/devices.

## 5) Common fixes if Google doesn’t pick it up

- Ensure `https://www.internitylabs.com/` resolves and is consistent (avoid mixed www/non-www).
- If you use both `internitylabs.com` and `www.internitylabs.com`, set a single canonical (already done in HTML) and configure your DNS/host to redirect the other to it.
- Add more indexable, query-relevant text to key pages (Products is the usual win).
