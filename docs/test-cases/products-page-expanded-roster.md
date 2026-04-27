# Expanded Products Page Roster Test Cases

## Scenario: Visitor sees newly approved products added
- **Given**: A visitor opens `/products` on closeforge.org
- **When**: The products page loads
- **Then**: They see SnapDesign, Resolved, and OpenClawMastermind in addition to the existing approved product cards
- **Edge case**: Existing approved products remain visible and ImpactMesh still does not appear

## Scenario: Expanded grid remains readable on mobile
- **Given**: A visitor opens `/products` on a phone-sized viewport
- **When**: They scroll through the expanded product grid
- **Then**: Each product card stacks in one column with readable badge, name, description, and CTA
- **Edge case**: No horizontal scrolling or clipped card content after increasing the roster size

## Scenario: Links and CTAs are safe for products without public URLs
- **Given**: Some products may not have a public landing page yet
- **When**: The visitor reads those cards
- **Then**: Cards use descriptive non-click CTAs instead of broken links
- **Edge case**: Public products keep working external links
