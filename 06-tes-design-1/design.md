# Test Design 1: Groups and Edges
**Tester:** Chinedu · **Date:** 10/27/2026
**Techniques:** equivalence partitioning, boundary value analysis
## About this project
(I used the equivalence partitioning and Boundary value analysis for the rules, what matters it testing if i can find a bug)
## Part 1: Practice rules
### Rule A: a password must be 8 to 16 characters
| Group | Valid or invalid | Value I would test |
|---|---|---|
| 0, 8-16, 17 | Invalid, Valid, Invalid | 0, 10, 17 |
**Edges:**
| Value | What should happen |
|---|---|
| 7, 8, 16, 17 | 7 should refuse, 8 should accept, 16 should accept, 17 should refuse  |
### Rule B: a transfer of ₦100 to ₦50,000
| Group | Valid or Invalid | Value I would test |
|---|---|---|
| ₦0, ₦100-₦50,000, ₦51,000 | Invalid, Valid, Invalid | 0, 500, 51,000 | 
**Edges:**
| Value | What should happen |
|---|---|
| ₦99, ₦100, ₦50,000, ₦51,000 | ₦99 should refuse, ₦100 should accept, ₦50,000 should accept, ₦51,000 should refuse | 
### Rule C: free delivery for orders of ₦10,000 or more
| Group | Valid or Invalid | Value I would test |
|---|---|---|
| ₦0, ₦10,000 or more | Invalid, valid |  0, 10,000, 15,000 |
**Edges:**
| Value | What should happen |
|---|---|
| ₦9,999, ₦10,000, | 9,999 should refuse, 10, 000 should accept |
