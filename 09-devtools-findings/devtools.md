# Developer Tools Findings
**Tester:** Chinedu · **Browser:** Chrome Phone on Laptop · **Date:** 11/4/2026
## About this project
(Two lines: what developer tools are, and what you used them for.)
* Developer tools are tools in a browser that help us check how a website works.
* I used them to check website pages, find errors and see if everything works properly.
 ## 1. Network: watch a search
- Request I found: https://automationexercise.com/products?search=top
- Status code: 200 (meaning: Everything is ok)
- Roughly how many requests for one page: 117
- What happened when I changed the address: The status shows 200, everything is fine and i got request 172 requests but indicate everything working properly 
- What this taught me: I learned how to use the Network tab to check requests and responses. 

<img width="2875" height="1627" alt="02-network-search" src="https://github.com/user-attachments/assets/3d45e631-d05f-404e-8222-0b2931389418" />
<img width="2875" height="1627" alt="02-network-search" src="https://github.com/user-attachments/assets/16e50f4f-20bb-4118-9582-172535fd2061" />

## 2. A product that does not exist
| Address | Expected | Actual | Status code | Bug or question |
|---|---|---|---|---|
| /product_details/99999 | Page not found | The page displayed with contents no picture and details shown | 200 | Bug |
| /abcxyz | Homepage appears | Redirected to homepage | 302 | Question |
**Bug report**
- Title: ____
- Steps: 1. ____
- Expected: ____
- Actual: ____
- Proof: ____
- Priority: ____ because ____
![Missing product](screenshots/02-missing-product.png)
