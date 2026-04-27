# Products Page with CoVyze Test Cases

## Scenario: Visitor sees approved CloseForge product roster
- **Given**: A visitor opens `/products` on closeforge.org
- **When**: The page loads
- **Then**: They see 8 product cards: LLM Council, RiseDaily, RiseOrPay, ScanFlow 掃帳, PawMatch, TapOK, GenSmith, and CoVyze
- **Edge case**: ImpactMesh must not appear anywhere on the products page

## Scenario: Mobile visitor can scan product cards cleanly
- **Given**: A visitor opens `/products` on a phone-sized viewport
- **When**: They scroll the page
- **Then**: Product cards stack in one column with readable names, badges, descriptions, and CTAs
- **Edge case**: No horizontal scrolling or clipped CTA text

## Scenario: Homepage links visitors to product roster
- **Given**: A visitor opens the CloseForge homepage
- **When**: They use the navigation or hero CTA
- **Then**: They can reach `/products`
- **Edge case**: Existing homepage layout and downloads remain intact
