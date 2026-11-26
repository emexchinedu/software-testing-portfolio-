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


