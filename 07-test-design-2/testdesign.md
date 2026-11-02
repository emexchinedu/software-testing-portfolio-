# Test Design 2: Rules, Memory and Smart Guesses
**Tester:** Chinedu · **Date:** 11/2/2026
## Assignment 1: Delivery fee table
| Question | Col 1 | Col 2 | Col 3 | Col 4 |
|---|---|---|---|---|
| Gold member? | Yes | Yes | No | No |
| Order ₦10,000 or more? | Yes | No | Yes | No |
| **What should happen** | Free(Discount) | Free | Free | ₦1,500 |
| ID | Column | Example customer | What should happen |
|---|---|---|---|
| TC-01 | 1 | Gold member | Gets free delivery and discount |
| TC-02 | 2 | Gold member | Gets free delivery | 
| TC-03 | 3 | Customer | Gets free delivery |
| TC-04 | 4 | Customer | Pays for the delivery |
**The column a tester would most likely forget:** Column 1 because the column meet the demands
## Assignment 2: SauceDemo login table
| Question | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
|---|---|---|---|---|---|
| Username typed? | Yes| Yes | Yes | Yes | No |
| Password typed? | Yes | Yes | Yes | No | Yes |
| Do they match? | Yes | Yes | No | No | No |
| Account locked? | Yes | No | Yes | Yes | No |
| **What should happen** | Locked  message | Logged in | Details do not match | Password required | Username required |
**A mix that cannot happen, and why:** The mix is not possible to happen, there's no rule for it and rules cant make for such. therefore its a bug
| ID | Column | What I typed | What should happen | What really happened (exact message) | Pass or Fail |
|---|---|---|---|---|---|
| TC-01 | 1 | Typed correct Username, password | Should Login | This user has been locked out | Fail |
| TC-02 | 2 | Typed correct details | Should login | logged to the product page | Pass |
| TC-03 | 3 | Typed incorrect details | Cant get through | Details do not match | Pass |
| TC-04 | 4 | Typed  correct username no password | Cant get through | Password is required | Pass |
| TC-05 | 5 | Typed correct password no username | Cant get through | Username is required | Pass | 
**Both boxes empty:** Username is required and its not much helpful, it should include password is required
![What it shows](saucedemo-login-fail.png)
![What it shows](saucedemo-login-pass.png)
## Assignment 3: Bank PIN
![My drawing](pin-drawing.jpeg)
| Where I am now | What I do | Where I end up |
|---|---|---|
| Ready | Wrong PIN | 1 wrong |
| Wrong PIN | 2 Wrong | Wrong PIN | 
| ID | Journey | What should happen | Should it be allowed? |
|---|---|---|---|
| TC-01 | Correct pin | logged in | Yes |
| TC-02 | Wrong, correct pin | Logged in | Yes |
| TC-03 | Wrong, Wrong, Correct | Logged In | Yes |
| TC-04 | Wrong, Wrong, Wrong | Locked | Yes |
| TC-05 | Wrong, Wrong, Wrong, Correct | Locked | No |
### Questions for the team
- If an account is locked after multiple failed login attempts, how long does the user have to wait before trying again?
- If an account is locked due to multiple failed login attempts, does the user need to reset their password to regain access, even if they enter the correct login credentials?
- ## Assignment 4: SauceDemo shopping trip
| Page I am on | What I click | Page I go to |
|---|---|---|
| Login page | Log in as standard_user | Products |
| Products | Add item to cart | product page showing items in the cart |
| products | Click the cart | Cart |
| Cart | Click on checkout | Checkout Information |
| Checkout | Type information | Checkout Overview |
 Checkout Overview | Click on finish | Complete
### Things that should be stopped
| ID | What I tried | What should happen | What really happened | Pass or Fail |
|---|---|---|---|---|
| TC-01 | log out paste the products page address back in | Goes back to login page | Login page appears | Pass |
| TC-02 | After Finish, press the browser Back button | Goes back to product | Goes back to checkout overview | Fail |
| TC-03 | Go to checkout with nothing in the cart | Cart page display without items | Cart page appears no item | Pass |
| TC-04 | Add items to cart, paste the cart page link in another browser | Same cart page with items appear | Same cart page with items appear | Pass |

![What it shows](saucedemo-trip.png)
## Assignment 5: Smart guessing
| # | Question | My guess | What I did | What happened | Bug, question or fine |
|---|---|---|---|---|---|
| 1 | Empty | If i click checkout leaving the boxes empty maybe i am logged to the account | at login leave the boxes empty and click login | Details are required | Fine |
| 2 | Wrong | If i enter numbers in place where letters are meant to be, maybe i can be able to login | Typed numbers in first name and last name's box | Checkout Overview appears | Bug |
| 3 | Edge | If i entered more digits expected in the box maybe it allows more digits | At the checkout information i added more number to the postal code | It allows more digits in the box | Question |
| 4 | Weird | If i enter emojis and symbols in first name box maybe i can use them to make a name | Checkout information add symbols as my name | Checkout overview appears | Bug |
| 5 | Twice |  If i double click finish maybe i order twice | After the checkout information i click finish twice | Checkout complete | Fine |
| 6 | Interrupt | If i refresh or lose internet halfway | Refresh the checkout information page | It comes back to the same page | Fine |
| 7 | Device | If i try with smaller screen phone maybe i will get the same view as on laptop | Used a small screen phone to view my checkout | The homepage was smaller and different | Question |
| 8 | | If I delay entering my correct details during checkout, maybe the system allow me to return and continue from where I stopped | On checkout page delay for sometime | It takes me back to the login page | Question |
| 9 | | If i enter the first name and postal code maybe it takes me to the checkout complete | At the checkout information enter details in first name and postal code | Displayed last name required | Fine |

**My most interesting result:** 8 	If I delay entering my correct details during checkout, maybe the system allow me to return and continue from where I stopped. It checks if the system saves your checkout progress when you take a long time to enter your details. If you return, can you continue from where you stopped without starting again?

