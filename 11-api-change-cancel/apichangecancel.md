## PART 1: PUT, PATCH, DELETE without key

| Order | Key | Expected | Actual | Status | Changed |
|---|---|---|---|---|---|
| PUT /https://restful-booker.herokuapp.com/booking/3226 | None | Should display 403 forbidden | Displayed 403 forbidden | 403 | No |
| PATCH /https://restful-booker.herokuapp.com/booking/3226 | None | Should display 403 forbidden | Display 403 forbidden | 403 | No |
| DELETE  /https://restful-booker.herokuapp.com/booking/3226 | None | Should display 403 Forbidden | Displayed 403 forbidden | 403 | No |
| PUT /https://restful-booker.herokuapp.com/booking/3226 | Made up | Should display forbidden | Displayed 403 forbidden | 403 | No |

- The requests were rejected, and nothing changed. The tests passed because the token and valid authentication token were not included in the request header.

- <img width="2523" height="1643" alt="PUT-booking-3226" src="https://github.com/user-attachments/assets/2169d26c-a929-4382-81b3-d11b64f6918c" />
- <img width="2863" height="1627" alt="PATCH-booking-3226" src="https://github.com/user-attachments/assets/f2dcce0d-a8a6-4899-b0cf-06cda2aa1c08" />
- <img width="2878" height="1631" alt="DELETE-booking-3226" src="https://github.com/user-attachments/assets/6392b37e-a0e0-408b-bcb4-243df1f0731d" />
- <img width="2859" height="1636" alt="PUT-booking-3226-madeup" src="https://github.com/user-attachments/assets/c9952676-677d-472a-8c2f-0a27096d856f" />


## PART 2: PUT, PATCH, DELETE with a key
| Order | Expected | Actual | Status |
|---|---|---|---|
| POST/https://restful-booker.herokuapp.com/booking | Display new booking with details and ID | New booking displayed with details and id | 200 |
| GET/https://restful-booker.herokuapp.com/booking/163 | Should Display the new booking | Displayed the new booking | 200 |
| PUT/https://restful-booker.herokuapp.com/booking/163 | Display new firstname and totalprice | Displayed booking with firstname and totalprice | 200 |
| GET/https://restful-booker.herokuapp.com/booking/163 | Display booking with new firstname and totalprice | Displayed the booking with new details | 200 |
| PATCH/https://restful-booker.herokuapp.com/booking/163 | Display the change from breakfast to dinner in the booking details | Booking details displayed dinner | 200 | 
| GET/https://restful-booker.herokuapp.com/booking/163 | Display the booking details with change to dinner | Displayed booking details with dinner | 200 |
| DELETE/https://restful-booker.herokuapp.com/booking/163 | Display CREATED 201 | Displayed CREATED 201 | 201 |
| GET/https://restful-booker.herokuapp.com/booking/163 | Display Invalid booking, not found | Displayed that the bookingid is mssing | 404 |

- The order DELETE/https://restful-booker.herokuapp.com/booking/163 displayed created 201 and its a question for the team. I checked if it has to end with a coma or to close it.

- <img width="2864" height="1638" alt="3-put-withkey" src="https://github.com/user-attachments/assets/2a7d7193-463c-422b-bc5c-66251b7d2fcf" />
- <img width="2857" height="1608" alt="5-patch-booking163" src="https://github.com/user-attachments/assets/60012616-4aca-4c3f-92ee-505dc89e7cb4" />
- <img width="2866" height="1629" alt="8-delete-booking163" src="https://github.com/user-attachments/assets/94b8a53a-2221-44ca-b233-8ac05f5696aa" />

## PART 3
| Try | What I Send | Tool | Expected | Actual | Status | Pass or Fail |
|---|---|---|---|---|---|---|
| 1 | DELETE /booking/{id} with key, then PATCH the same booking, body: {"firstname": "Josh"} | State | Display Method not allowed, Investigate 405 Method Not Allowed | Displayed Method not allowed, Investigate 405 Method Not Allowed | 405 | Pass |
| 2 | PATCH: {"firstname": ""} with key | Smart Guessing Empty | Should display bad request 400 | Displayed the booking bad request | 400 | Pass |
| 3 | PATCH: {"totalprice": 0} with key | Edges | Should display bad request | Displayed the booking with totalprice 0 | 200 | Fail |
| 4 | PATCH: {"totalprice": "abc"} | Smart Guessing Wrong | Should Display forbidden  | Displayed Fix 403 Forbidden error | 403 | Pass |

- Bug report : PATCH: {"totalprice": 0} with key
- Title: Booking with no totalprice
- Request: PATCH/bookingid/header<valid token>/Body
- Expected: Should display bad request
- Actual: Displayed the booking with totalprice 0
- Priority: Highest
- Proof: <img width="2861" height="1653" alt="patch-totalprice0" src="https://github.com/user-attachments/assets/20084d5d-815c-4df8-9a83-d2dfc7bb2733" />


