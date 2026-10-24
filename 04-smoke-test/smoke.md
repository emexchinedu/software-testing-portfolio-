# Smoke Test: SauceDemo
**Date:** 10/23/2026 · **Browser:** Chrome
| # | Step | Expected | standard_user | problem_user |
|---|---|---|---|---|
| 1 | Open the site | Login page appears | Pass | Pass |
| 2 | Enter correct details in login input fields | Homepage appears | Pass | Pass |
| 3 | Open the homepage | Pictures match the product content | Pass | Fail |
| 4 | Click on a product | Product page display the content and price | Pass | Fail |
| 5 | Click on filtered Button and select | Products displayed what was meant to filter | Pass | Fail |
| 6 | Open the homepage | All products can add to cart | Pass | Fail |
| 7 | Open the homepage | All products can remove from cart | Pass | Fail |
| 8 | Open a product page, at left side of the bottom page, click any of the social media button | It navugates to the social media page to login | Pass | Pass |
| 9 | Products added to cart, click the checkout | It should navigate to payment instructions | Pass | Fail |
| 10 | Stay on the account for 5 seconds without activity |The page logs out to input the user correct details | Pass | Pass | 
## Decision
- **standard_user:** ready for deeper testing because bugs are low, we can be fixed and retest
- **problem_user:** send it back because bugs are high, we needs urgent attention
## Evidence
![What the picture shows](screenshots/smoke-problem-user-xxx.png)
