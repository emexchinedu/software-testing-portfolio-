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
|


