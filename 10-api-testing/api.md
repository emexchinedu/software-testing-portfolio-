## GET ORDER
| Order | Expected | Actual | Status | Time |
|---|---|---|---|---|
| GET /ping | Should Display Created and successfully | Displayed created and successfully | 201 | 1.95 s |
| GET /booking | Should display the list of the bookings | Displayed the list of the bookings | 200 | 313 ms |
| GET /booking/5 | Booking 5 details display | Details about booking 5 appears | 200 | 312 ms | 
| GET /booking/999999 | Should display error code | Not found appears | 404 | 321 ms |
| GET /booking/hello | Should display error code | Not found appears | 404 | 1.89 s |
<img width="2878" height="1681" alt="booking-5" src="https://github.com/user-attachments/assets/465ab15b-9643-466a-852b-3294988cf205" />
<img width="2798" height="1680" alt="booking-999999" src="https://github.com/user-attachments/assets/b41ea162-4e4a-4dbc-a40c-e68eafaed83e" />



## POST ORDER
| Booking | Bookingid | POST status | GET status | Everything matches? (yes /no) |
|---|---|---|---|---|
| 1 | 323 | 200 | 200 | Yes |
| 2 | 2536 | 200 | 200 | Yes |

## 10 Tries
| Try | What i change | Tool i used | Expected | Actual | Status | Pass or Fail |
|---|---|---|---|---|---|---|
| 1 | Leave totalprice empty | Edge | 400 and bad request should display | 400 and bad request displayed | 400 | Pass |
| 2 | Put numbers in firstname | Smart guessing | Should display bad request | The numbers appeared on the firstname clearly | 200 | Fail |
| 3 | Put -100 in totalprice | Edge | 400 and bad request should display | Booking Details Displayed successfully with -100 | 200 | Fail |
| 4 | Leave firstname empty | Smart guessing | 400 and bad request should display | Booking Details Displayed successfully with no firstname | 200 | Fail |
| 5 | Enter letters in totalprice | Group | 400 and bad request should display | 400 and bad request displayed | 400 | Pass |
| 6 | Leave depositpaid empty | Smart guessing | 400 and bad request should display | 400 and bad request should display | 400 | Pass |
| 7 | Change checkin date to Letters | Group | 400 and bad request should display | Booking Details displayed successfully with letters | 200 | Fail |
| 8 | Change checkout date to letters | group | 400 and bad request should display | Booking Details displayed successfully with letters | 200 | Fail |



