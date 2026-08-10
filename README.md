# Boat Lane Paddock

Static website for [Boat Lane Paddock](https://boatlaneglamping.co.uk), a private group-glamping site in Worcestershire.

## Publishing

The site is hosted on GitHub Pages from the `main` branch's `/docs` folder.

- Live site: <https://boatlaneglamping.co.uk>
- GitHub Pages source: `main` → `/docs`
- Custom-domain file: `docs/CNAME`

Do not change the existing DNS records as part of normal website updates. Merge an approved pull request into `main`; GitHub Pages will publish the updated `/docs` contents.

## Site structure

```text
docs/
├── index.html                 # Scrollable homepage
├── group-glamping/index.html  # Focused group-stays page
├── team-retreats/index.html   # Focused team-retreats page
├── soundfulness/index.html    # Focused Soundfulness page
├── landing-pages.css          # Shared styles for the focused pages
├── robots.txt                 # Crawler instructions
├── sitemap.xml                # URLs submitted to search engines
└── *.jpg / *.JPG              # Site images
```

The homepage remains the complete, scrolling overview. The three focused pages are supplementary routes that are linked from the relevant homepage sections and link back to the homepage and to one another.

## Theme toggle

The homepage includes a Meadow / Night toggle beside the main navigation. It retains the original green banners while switching the light page surfaces to near-black forest green. The visitor's choice is saved in their browser.

## Image rules

GitHub Pages is case-sensitive. Image references must match the committed filename exactly—for example, `popout001.JPG` is different from `popout001.jpg`.

The visible content images open the gallery at their matching full-size image. Add any new image to the gallery list in `docs/index.html` if it should be gallery-enabled.

## SEO

The site includes page-specific titles, descriptions, canonical URLs, Open Graph metadata, JSON-LD, `robots.txt`, and `sitemap.xml`.

After a future deployment:

1. Add `https://boatlaneglamping.co.uk/sitemap.xml` to Google Search Console.
2. Use Google Search Console's URL Inspection for the homepage and each focused page.
3. Create and verify the Google Business Profile with the business's exact public name, address or service area, contact details, category, hours, and photos.
4. Once the Google Business Profile exists, add its verified public URL to the site's structured data.

Do not add an address, opening hours, map coordinates, or review rating to the website's structured data unless those are verified, current business facts.

## Local checks

Before committing, at minimum verify:

```powershell
git diff --check
```

Also check that each new route has an `index.html`, a matching canonical URL, a sitemap entry, working navigation, and exact-case asset paths.
