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

## 3. Where SauceDemo remembers you
- Was there a login request? ____ What I saw instead: ____
- Cookie name and value: Session, Standard_user
- What the second drawer (Local Storage) showed after adding the backpack: Cart contents [4]
- What happened when I deleted the cookie: The session and standard_user name and value were cleared, leaving them empty. When I refreshed the page, it redirected me to the login page.
- Why a real shop must work differently: to prevent attackers, make bugs easier to detect, and fix them quickly.
<img width="2859" height="1611" alt="03-cookie" src="https://github.com/user-attachments/assets/4010f488-c1a3-4bb9-845e-50832b16b934" />

## 4. Console errors with error_user
| Product | Added? | Console message |
|---|---|---|
| Sauce Labs Backpack | Yes |  |
| Sauce Labs Bike Light | Yes | 
| Sauce Labs Onesie | Yes |

**Bug 1:** Title: Filter button broken. Steps: On the homepage, click on the filter button, click (Name Z to A). Expected: Items should be displayed in alphabetical order, from Z to A. Actual: Message pops up showing its broken. Proof: <img width="2355" height="1617" alt="Screenshot 2026-11-15 115906" src="https://github.com/user-attachments/assets/ac7c5d2a-9a6c-4665-8a65-8c4b2d810855" />
 Priority: Medium

**Bug 2:** Falied to add and remove from cart, Steps: on the homepage, click on an item to cart and remove from cart, Expected: Item should be added to cart and remove from cart, Actual: Added items cant be remove from cart and items cant add to cart, Proof: <img width="2871" height="1613" alt="Screenshot 2026-11-15 123148" src="https://github.com/user-attachments/assets/c261a34f-33d9-4b24-a1f7-fc05368a7c5f" />
, Priority: High

![Console](screenshots/04-console.png)

## 5. Phone size and slow network
| Check | Device or speed | What I saw | Problem? |
|---|---|---|---|
| SauceDemo checkout | iPhone 12 Pro | Mobile version displayed | No |
| SauceDemo checkout | Galaxy S20, sideways | Mobile Version displayed | No |
| automationexercise products | 3G | Finish: 12.29 seconds | Yes |
<img width="2845" height="1606" alt="05-phone" src="https://github.com/user-attachments/assets/ab08b272-d24d-4e66-a129-c1e8eefef391" />

<img width="2857" height="1641" alt="05-slow" src="https://github.com/user-attachments/assets/616f30ae-eab2-42ad-906c-24b1e2500242" />

