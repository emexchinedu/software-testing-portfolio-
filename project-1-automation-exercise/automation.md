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
### 5. Devices and browsers Laptop, Phone and Chrome, safari
### 6. What could go wrong (risks) If customer forgets the username and password, Entering the incorrect details, Customer cant see the product page
### 7. When I stop, when the bugs are gone

| ID | What it checks | Tool | Test data | Steps | Expected | Actual | Pass or Fail |
|---|---|---|---|---|---|---|---|
| TC-01 | Register with valid details | Group | Name: Phil, email: phil@gmail.com  | On signup/login page Enter a name, Click sign up | It goes to enter account information | It goes to enter account information | Pass |
| TC-02 | Register using an existing email | Group | using same email to register a new account | On signup/login page Enter a name and an email address that is already registered. Click Signup | Displays the email address already exists | Displays an error message that the email address already exists | Pass |
| TC-03 | Login with correct details and logout | Decision table | Email: phil@gmail.com password: 1234567890 | On signup/login page Enter a registered email and correct password. Click Login, then Logout | User logs in successfully and is returned to the login page after logout | User logs in successfully and is returned to the login page after logout | Pass |
| TC-04 | Login with incorrect details | Decision table | Email: philgmail.com password: 48493444 | On signup/login page Enter an incorrect email address or password. Click Login | Displays your email or password is incorrect | Displays your email or password is incorrect | Pass |
| TC-05 | Search for an existing product | Smart guessing | Search the item dress | on the homepage, click on products, click on search, enter the term dress, click on search | Dress products are displayed | Dress products are displayed | Pass |
| TC-06 | Search for a product that does not exist | Smart guessing | Search term 1234563=--- | On the homepage, click on products, enter the term 1234563=---, click on search | No matching products are displayed | Search products empty | Pass |
| TC-07 | View products details | Smart guessing | product blue top | click on products and search for blue top, click on view product | Product details, price, description, and quantity options are displayed correctly | Details about the product appears | Pass |




