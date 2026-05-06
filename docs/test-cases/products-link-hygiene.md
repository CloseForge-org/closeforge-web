# Products Link Hygiene Test Cases

## Scenario: Product visitor only sees working external links
- **Given**: A visitor opens `/products` on closeforge.org
- **When**: They click product CTAs
- **Then**: Public products with verified URLs open normally, while products without working public URLs show non-click Coming Soon/private-beta CTAs
- **Edge case**: Previously broken RiseDaily, ScanFlow, and PawMatch links must not remain clickable

## Scenario: Contact action avoids Cloudflare email-protection 404s
- **Given**: A visitor wants to contact CloseForge
- **When**: They use the nav/footer/contact CTA
- **Then**: The contact action opens a normal composed email to roger@closeforge.org instead of a Cloudflare `/cdn-cgi/l/email-protection` URL
- **Edge case**: Static link checking must not report a broken Cloudflare email-protection route

## Scenario: Homepage and products page stay consistent
- **Given**: A visitor sees product links on either the homepage or `/products`
- **When**: They inspect CTAs for the same product roster
- **Then**: Both pages avoid the same known-broken product URLs
- **Edge case**: Verified working links like VerdictAI, RiseOrPay, CoVyze, and SnapDesign remain clickable
