# Use Case Model

**Author**: Team047

## 1 Use Case Diagram

![Use case](./useCaseDiagram.png)

## 2 Use Case Descriptions

### Current Job Entry

- Requirements 
  - Allow user to add job details.
- Pre-conditions
  - User is in job entry page.
- Post-conditions
  - Job details are saved to database
- Scenarios:
  - Normal
    - User enters job details
    - User chooses to save job, and job details are saved to database. 
  - Alternate
    - User chooses to cancel, then UI goes back to main UI without doing anything.	      

### Offer Entry

- Requirements
  - Allow user to add offer details.
- Pre-conditions
  - User is in offer entry page.
- Post-conditions
  - Offer details are added to database. 
- Scenarios:
  - Normal
    - User enters offer details.
    - User chooses to save offer, and offer is saved to database.
  - Alternate
    - User chooses to canel, then UI goes back to main UI without doing anything.

### Compare Job and Offer

- Requirements
  - Allow user to comapre to job after entering an offer.
- Pre-conditions
  - User enters one offer and job detail is present.
- Post-conditions
  - A comparison between job and offer is displayed to user.
- Scenarios:
   - User enters offer information.
   - User chooses to compare with job.
   - Job and comparison settings are pulled from database.
   - Job and offer are compared and displayed to user.

### Comparison Settings Entry

- Requirements
  - Allow user to adjust comparison settings.
- Pre-conditions
  - User is in comparison adjustment page.
- Post-conditions
  - Comparison settings are added to database. 
- Scenarios:
  - Normal
    - User enters comparison settings.
    - Comparison settings are saved to database.

### Compare Selected Job/Offers

- Requirements
  - Show user a list of ranked offers/job.
- Pre-conditions
  - User is in compare offer page.
- Post-conditions
  - A list of ranked offers/jobs is displayed to user. 
- Scenarios:
  - Normal
    - job and offer detail is pulled from database.
    - Comparison settings are pulled from database.
    - Job and offer scores are calculated.
    - Job and offers are sorted by score.
    - A list is displayed to user.
  - Exception
    - Job and offer database is empty and there is nothing to calculate and display.

### Select and compare two jobs

- Requirements
  - Allow user to select two job/offers from the list and compare them
- Pre-conditions
  - User is in compare offer page and list of job/offers are ranked and displayed.
- Post-conditions
  - A comparison between selected job/offers is displayed to user.
- Scenarios:
  - Normal
    - Two job/offers are selected.
    - job/offer details are pulled from database.
    - Job/offer are compared and displayed to user.
  - Exception
    - There is less than two job/offer available in database. User is not able to compare.