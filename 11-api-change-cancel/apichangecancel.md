## PART 1: PUT, PATCH, DELETE without key

| Order | Key | Expected | Actual | Status | Changed |
|---|---|---|---|---|---|
| PUT /https://restful-booker.herokuapp.com/booking/3226 | None | Should display 403 forbidden | Displayed 403 forbidden | 403 | No |
| PATCH /https://restful-booker.herokuapp.com/booking/3226 | None | Should display 403 forbidden | Display 403 forbidden | 403 | No |
| DELETE  /https://restful-booker.herokuapp.com/booking/3226 | None | Should display 403 Forbidden | Displayed 403 forbidden | 403 | No |
| PUT /https://restful-booker.herokuapp.com/booking/3226 | Made up | Should display forbidden | Displayed 403 forbidden | 403 | No |

- The requests were rejected, and nothing changed. The tests passed because the token and valid authentication token were not included in the request header.

<img width="2523" height="1643" alt="PUT-booking-3226" src="https://github.com/user-attachments/assets/2169d26c-a929-4382-81b3-d11b64f6918c" />
<img width="2863" height="1627" alt="PATCH-booking-3226" src="https://github.com/user-attachments/assets/f2dcce0d-a8a6-4899-b0cf-06cda2aa1c08" />
<img width="2878" height="1631" alt="DELETE-booking-3226" src="https://github.com/user-attachments/assets/6392b37e-a0e0-408b-bcb4-243df1f0731d" />
<img width="2859" height="1636" alt="PUT-booking-3226-madeup" src="https://github.com/user-attachments/assets/c9952676-677d-472a-8c2f-0a27096d856f" />


## PART 2: 
| Order | Expected | Actual | Status |
|---|---|---|---|
| POST/https://restful-booker.herokuapp.com/booking | Display new booking with details and ID | New booking displayed with details and id | 200 |
| GET/https://restful-booker.herokuapp.com/booking/163 | Should Display the new booking | Displayed the new booking | 200 |
| PUT/https://restful-booker.herokuapp.com/booking/163 | Display new firstname and totalprice | Displayed booking with firstname and totalprice | 200 |
| GET/https://restful-booker.herokuapp.com/booking/163 | Display booking with new firstname and totalprice | Displayed the booking with new details | 200 |
| PATCH/https://restful-booker.herokuapp.com/booking/163 | Display the change from breakfast to dinner in the booking | Booking displayed dinner | 200 | 
