## Project 1: Manual Test of Automation Exercise
| Part of the shop | What it does | If it broke, which M? |
|---|---|---|
| Click sign up | It allows new user to register in the website | Money(critical) |
| Login Button | It allows registered user to get in the website to do shopping | Money(critical) |
| Contact us | It allows user to contact the company, if the user have problem or questions | Makeup(low) |
| Click Product and products detail page | It allows user to see the product and its content on what to shop | Money(critical) |
| Search Product | It allows customer to search for a specific product to shop | Mission(high) |
| Add products in cart | It allows customer to select a product and add to cart for checkout and place order | Money(critical) |
| Remove product from cart | It allows customer to remove items from the cart if customer makes another choice | Money(critical) |
| Click category products | It makes it easier for customer to select items to shop | Medium |
| Check product quantity in cart | It allows customer to select number of items | Money(critical) |
| Checkout button | It allows customer to checkout the products from the cart | Money(critical) |
| Place order Button | It allows customers to place an order at checkout using the information they have provided | Money(critical) |

## Test Plan
### 1. What I will test, sign up, login, Products page and details, add and remove items from cart, search products, number of items in the cart to reduce or add more, checkout, place order
### 2. What I will not test the video tutorials and why because whatever information that comes from it is not the part of the testing
### 3. Who, tester
### 4. When, 11/8/2026 to 11/10/2026
### 5. Devices and browsers Laptop, Chrome
### 6. What could go wrong (risks) If customer can be overcharged when a cart total is wrong from the website
### 7. When I stop, when all 20 tests have run and every fail is in jira

| ID | What it checks | Tool | Test data | Steps | Expected | Actual | Pass or Fail |
|---|---|---|---|---|---|---|---|
| TC-01 | Register with valid details | Group | Name: Phil, email: phil@gmail.com  | On signup/login page Enter a name, Click sign up | It goes to enter account information | It goes to enter account information | Pass |
| TC-02 | Register using an existing email | Group | using same email to register a new account | On signup/login page Enter a name and an email address that is already registered. Click Signup | Displays the email address already exists | Displays an error message that the email address already exists | Pass |
| TC-03 | Login with correct details and logout | Decision table | Email: phil@gmail.com password: 1234567890 | On signup/login page Enter a registered email and correct password. Click Login, then Logout | User logs in successfully and is returned to the login page after logout | User logs in successfully and is returned to the login page after logout | Pass |
| TC-04 | Login with incorrect details | Decision table | Email: philgmail.com password: 48493444 | On signup/login page Enter an incorrect email address or password. Click Login | Displays your email or password is incorrect | Displays your email or password is incorrect | Pass |
| TC-05 | Search for an existing product | Smart guessing | Search the item dress | on the homepage, click on products, click on search, enter the term dress, click on search | Dress products are displayed | Dress products are displayed | Pass |
| TC-06 | Search for a product that does not exist | Smart guessing | Search term 1234563=--- | On the homepage, click on products, enter the term 1234563=---, click on search | No matching products are displayed | Search products empty | Pass |
| TC-07 | View products details | Smart guessing | product blue top | click on products and search for blue top, click on view product | Product details, price, description, and quantity options are displayed correctly | Details about the product appears | Pass |
| TC-08 | Refuse zero product quantity | Edges | quantity 0 | On a product page select quantity 0 and add to cart | System refuses to add a zero-quantity product to the cart | Product doesn't go beyond 1 | Pass |
| TC-09 | Increase product quantity | Edges | Quantity 2 | On a product page select quantity 2 and add to cart | Cart accepts quantity 2 and total the correct price of the two | Product displayed two items added and total price | Pass |
| TC-10 | Remove a product from cart | Edges | A product in the cart | On a product page, add product to the cart and remove product from the cart | Product is removed and the cart is updated accordingly | the cart is empty | Pass |
| TC-11 | Add one product to cart | Edges | Add a product to cart | On product page, click add to cart | Product appears in the cart with a correct price | Product appears in the cart with a correct price | Pass |
| TC-12 | Refuse any ch | Group | Add more quantity to know exceeding number | Product page, add product to cart, click quantity, it doesn't show any exceeding number | Should show the maximum you can purchase | Adding more numbers, the cart button doesn't work | Fail |
| TC-13 | Checkout as a logged-in user | States | Registered user product in cart | Log in, Add product to cart, Click Proceed to Checkout | User information displayed to place order | Delivery address and billing address appears to place order | Pass |
| TC-14 | Refuse checkout without login | States | Product in cart user logged out | Add product to cart, Log out, Open cart, Click Proceed to Checkout | System requests the user to log in or register before proceeding with checkout | Login/signup page pops up | Pass |
| TC-15 | Complete payment with valid details | Smart guessing | Valid name, card number, expiry date, and CVV | Add product to cart, click on checkout, fill the payment information to pay | Payment is accepted, confirmation message displayed | Cant entered the payment information without clicking confirm for each box | Fail |
| TC-16 | Refuse payment with missing required details | Smart guessing | Missing card number or CVV | Add to cart, click checkout, filling the payment information and miss a number, click pay and confirm | Payment is refused and the system displays a validation message, order is not confirmed | It shows order has been placed successfully | Fail |
| TC-17 | Submit Contact Us form successfully | Smart guessing | Name, Email, Message | On the homepage click on contact us, enter name, email, message click on submit | Contact form is submitted successfully and a success message is displayed | Success! Your details have been submitted successfully appears | Pass |
| TC-18 | Refuse Contact Us form with missing required fields | Smart guessing | No Name, no Message | On the homepage click on contact us, leave box empty for name, email, message click on submit | System refuses the incomplete submission and displays validation feedback |  The boxes require details to be filled |  Pass |
| TC-19 | Subscribe using a valid email | Group | Valid email | Scroll to bottom of the page, entered valid email in the subscription box, click on submit | User is successfully subscribed and a success message is displayed | You have been subscribed successfully appears | Pass |
| TC-20 | Refuse invalid email | Group | Invalid email | Scroll to bottom of the page, entered invalid email in the subscription box, click on submit | System refuse the invalid email and does not subscribe the user | It requires correct email to subscribe | Pass | 

## Question for the team
Is there a maximum quantity of stock that a customer can purchase?

## Bugs
| Jira | Summary | Found by | Priority | Why this priority |
|---|---|---|---|---|
| AET-1 | Refuse quantity exceeding available stock, Steps: Product page, add product to cart, click quantity, it doesn't show any exceeding number, Expected: Should show the maximum you can purchase, Actual: Adding more numbers, the cart button doesn't work, Browser: Chrome(incognito), Laptop | TC-12 | Highest | User doesn't have limit to purchase |
| AET-2 | Complete payment with valid details, Steps: Add product to cart, click on checkout, fill the payment information to pay, Expected: Payment is accepted, confirmation message displayed, Actual: Cant entered the payment information without clicking confirm for each box, Browser: Chrome(incognito), Laptop | TC-15 | Highest | User cant be able make purchase without filling the payment details |
| AET-3 | Order placed with a wrong card number, Steps: Add to cart, click checkout, filling the payment information and miss a number, click pay and confirm, Expected: Payment is refused and the system displays a validation message, order is not confirmed, Actual: It shows order has been placed successfully, Browser: Chrome(incognito), Laptop | TC-16 | Highest | Order can placed even with incorrect payment details | 

<img width="2523" height="1464" alt="tc-16-payment" src="https://github.com/user-attachments/assets/e8718a97-b00e-438f-9e9e-cac78f64634b" />
<img width="2210" height="1219" alt="tc-15-payment" src="https://github.com/user-attachments/assets/685e85a5-b5f4-48f2-aea2-905154266ad7" />
<img width="2723" height="1459" alt="tc-12-quantity" src="https://github.com/user-attachments/assets/e0324853-858b-4cad-ad05-b03eb050c77e" />






## Summary
Tested: Automation Exercise · Browser: chrome(Incognito) · Date: 11/8/2026
Test cases: 20 written · 20 run · 17 passed · 3 failed
Bugs in Jira: AET-1, AET-2, AET-3, Highest 3 
Most serious bug: AET-1 because user wont be able to make purchase from the website
Questions for the team: Can the website be on timeout for registered users? 
My recommendation: not ready, because the checkout system still needs to be fix and retest
Next time I would: I will retest the checkout system and available quantity a customer can purchase

## What I learned
I learned how to test different parts of a website and make sure they work properly
-I learned how to find bugs and report them on Jira for developers to fix
-I learned how to to check test results and know when a website is ready for users





