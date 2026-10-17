# Pittsburgh Pool Company legacy URL / NAP cleanup

Updated 2026-09-26

Public search still exposes legacy pages using old phone/address information. These should be 301 redirected when the GoDaddy production deployment is updated so existing authority is preserved rather than deleted.

## Known legacy URLs and recommended targets

- `/inground-pool-installation` → `/inground-pools-pittsburgh-pa.html`
- `/pool-maintenance-and-service` → `/service.html`
- `/pool-openings-and-closings` → `/service.html`
- `/pool-covers` → `/service.html` or a future dedicated pool-cover page
- `/pool-chemicals` → `/service.html` or a future water-care page
- `/about` → `/index.html` unless a new About page is created
- `/contact` → `/contact.html`
- `/outdoor-living` → preserve only if this is intentionally still offered on PGHPoolco; otherwise redirect to the correct HTFO outdoor-living destination
- `/above-ground-pools` → redirect to `/inground-pools-pittsburgh-pa.html` or a clear current pool-options page because above-ground pools were removed from the new site strategy

## NAP cleanup

Legacy pages are still publishing phone `412-228-3595` and some third-party citations also expose older numbers/addresses. As confirmed by Ray on 2026-10-17, use `412-326-0361` for Pittsburgh Pool Company and the HTFO family showroom addresses:

- 4680 Old William Penn Highway, Suite 205, Monroeville, PA 15146
- 10269 Perry Highway, Wexford, PA 15090

Approved public numbers (Ray, 2026-10-17): `412-326-0361` and `1-888-8-HOTTUB` (`888-846-8882`). Replace all other business contact numbers, including former agency tracking numbers, across websites, Google Business Profiles, directories and chambers. Former tracking numbers no longer route to the business.

## Deployment requirement

The new local SEO files are committed in GitHub but are returning 404 from production. The GoDaddy production site needs a deployment/sync of the current repository before the local pages, new Learning Center articles, sitemap changes and robots.txt can be crawled.

## Redirect implementation

Use server-side HTTP 301 redirects on the production host. Do not rely on JavaScript or meta-refresh redirects when a server redirect is available. Keep redirects one-to-one where a close replacement exists and avoid redirect chains.
