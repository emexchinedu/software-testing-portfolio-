## GET ORDER
| Order | Expected | Actual | Status | Time |
|---|---|---|---|---|
| GET /ping | Should Display Created and successfully | Displayed created and successfully | 201 | |
| GET /booking | Should display the list of the bookings | Displayed the list of the bookings | 200 | |
| GET /booking/5 | Booking 5 details display | Details about booking 5 appears | 200 | | 
| GET /booking/999999 | Should display error code | Not found appears | 404 | |
| GET /booking/hello | Should display error code | Not found appears | 404 | |

## POST ORDER
| Booking | Bookingid | POST status | GET status | Everything matches? (yes /no) |
|---|---|---|---|---|
| 

