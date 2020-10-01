# Use Case Model

**Author**: Team047

## 1 Use Case Diagram

![Use case](./useCaseDiagram.png)

## 2 Use Case Descriptions

### Current Job Entry

- Requirements 
  - Allow user to add job details.
- Pre-conditions
  - User is in job entry UI.
- Post-conditions
  - Job details are added to database
  - User returns to main page without saving.
- Scenarios:
  - User enters job description.
  - If user chooses to save job, job description is saved to database. If user chooses to cancel, UI goes back to main UI without doing anything.	      

Offer Entry

 - Requirements: Allow user to add offer details.
 - Pre-conditions: User is in offer entry UI.
 - Post-conditions: Offer details are added to database, or user returns to main page without saving.
 - Scenarios:
   1. User enters inputs job description.
   2. If user chooses to save job, job description is saved to database. If user chooses to cancel, UI goes back to main UI without doing anything.

Comparison Settings Entry

Compare Selected Job/Offers



- *Requirements: High-level description of what the use case must allow the user to do.*
- *Pre-conditions: Conditions that must be true before the use case is run.*
- *Post-conditions Conditions that must be true once the use case is run.*
- *Scenarios: Sequence of events that characterize the use case. This part may include multiple scenarios, for normal, alternate, and exceptional event sequences. These scenarios may be expressed as a list of steps in natural language or as sequence diagrams.*