# Remove KamaQuotient Test Cases

## Scenario: Homepage no longer advertises KamaQuotient
- **Given**: A visitor opens the CloseForge homepage
- **When**: They scan the product grid
- **Then**: KamaQuotient is not shown anywhere on the page
- **Edge case**: Nearby product cards still render correctly after the removal

## Scenario: Remaining product grid content is intact
- **Given**: A visitor opens the CloseForge homepage
- **When**: They review products before and after the removed card position
- **Then**: PawMatch, MIDAIS, and Resolved remain visible with their descriptions
- **Edge case**: No broken HTML or dangling product-card block remains
