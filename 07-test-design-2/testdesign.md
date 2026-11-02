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
![My drawing](screenshots/pin-drawing.jpg)
| Where I am now | What I do | Where I end up |
|---|---|---|
| Ready | Wrong PIN | 1 wrong |
| | | |
| ID | Journey | What should happen | Should it be allowed? |
|---|---|---|---|
| | | | |
### Questions for the team
- ____
- ____
