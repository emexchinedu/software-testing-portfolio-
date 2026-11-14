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
| /product_details/99999 | 404 Page Not Found error should appear | The page displayed with contents no picture and details shown | 200 | Bug |
| /abcxyz | 404 Page Not Found error should appear | website redirects to the homepage and displays the website content | 302 | Bug |
**Bug report**
- Title: Invalid URL redirects to the homepage
- Steps: 1.Open the browser 2. Enter https://automationexercise.com/abcxyz in the address bar 3. Press Enter.
- Expected: A 404 Page Not Found error should appear because the URL does not exist.
- Actual: Website redirects to the homepage and displays the website content
- Proof: <img width="2850" height="1559" alt="300" src="https://github.com/user-attachments/assets/57dd1d2a-4c81-4321-85f7-fca7e6e77ae1" />

- Priority: Low because it redirected back to the main webiste
<img width="2870" height="1300" alt="02-missing-product" src="https://github.com/user-attachments/assets/1b45c96e-09cd-4eff-af4a-b7ff6929d2c7" />

