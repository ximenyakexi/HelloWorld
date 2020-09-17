# **Design Description**
## **Requirements & Description**
1. *When the app is started, the user is presented with the main menu, which allows the user to (1) enter current job details, (2) enter job offers, (3) adjust the comparison settings, or (4) compare job offers (disabled if no job offers were entered yet).*

 **This is not included in the design as required by assignment. It is purely GUI-specific class.**

2. *When choosing to enter current job details, a user will:*

 a. *Be shown a user interface to enter (if it is the first time) or edit all of the details of their current job, which consist of:*
  1. *Title*
  2. *Company*
  3. *Location (entered as city and state)*
  4. *Overall cost of living in the location (expressed as an index)*
  5. *Commute time (round-trip and measured in hours or fraction thereof)*
  6. *Yearly salary*
  7. *Yearly bonus*
  8. *Retirement benefits (as percentage matched)*
  9. *Leave time (vacation days and holiday and/or sick leave, as a single overall number of days)*

  **User interface is not included in the design.**

  **Class "Job" contains attributes for job details. An extra attribute "isCurrent" is added to differ current job from offers. As discussed in 3.a, another class "CurrentJob" implements "Job" which holds current job information.**

 b. *Be able to either save the job details or cancel and exit without saving, returning in both cases to the main menu.*

  **Add saveJob() method to class "Job" to save job details into database. Database support layer is not included**
  **Cancel and exit functions are not included since user interface is not included in the design.**

3. *When choosing to enter job offers, a user will:*

 a. *Be shown a user interface to enter all of the details of the offer, which are the same ones listed above for the current job.*

  **User interface is not included in the design.**
 
  **Class "Offer" implements class "Job" and contains offer details. Another Class "CurrentJob" also implements class "Job". Current job and offer have two different classes because they may have different methods and attributes in the future if requirements changed.**

 b. *Be able to either save the job offer details or cancel.*

  **Class "Offer" inherits saveJob() method from class "Job".**

  **User interface is not included in the design.**

 c. *Be able to (1) enter another offer, (2) return to the main menu, or (3) compare the offer with the current job details (if present).*

  **User interface is not included in the design.**

  **Compare job and offer will be discussed in requirement 5.**

4. *When adjusting the comparison settings, the user can assign integer weights to:*

 a. *Commute time*

 b. *Yearly salary*

 c. *Yearly bonus*

 d. *Retirement benefits*

 e. *Leave time*

 *If no weights are assigned, all factors are considered equal.*

 **Class "ComaparisionSetting" holds comparison settings. Settings are initialized to 1. Weighted settings are added to attributes too.**

5. *When choosing to compare job offers, a user will:*

 a. *Be shown a list of job offers, displayed as Title and Company, ranked from best to worst (see below for details), and including the current job (if present), clearly indicated.*

 **User interface is not included in the design.**

 **Class "JobComparison" has method listJobOffer() to pull jobs from database and rank jobs.**

 b. *Select two jobs to compare and trigger the comparison.*

 **Class "JobComparison" has method selectJob() to select two jobs.**

 c. *Be shown a table comparing the two jobs, displaying, for each job:*

 **User interface is not included in the design.**

 **Class "JobComparison" has method compareJob() to compare selected jobs.**

  1. *Title*
  2. *Company*
  3. *Location*
  4. *Commute time*
  5. *Yearly salary adjusted for cost of living*
  6. *Yearly bonus adjusted for cost of living*
  7. *Retirement benefits (as percentage matched)*
  8. *Leave time*

 d. *Be offered to perform another comparison or go back to the main menu.*

 **User interface is not included in the design.**

6. *When ranking jobs, a job’s score is computed as the weighted sum of:*

 *AYS + AYB + (RBP * AYS) + (LT * AYS / 260) - (CT * AYS / 8)*

 **Implementation is not included in the design.**

7. *The user interface must be intuitive and responsive.*

 **Implementation is not included in the design.**

8. *The performance of the app should be such that users do not experience any considerable lag between their actions and the response of the app.*

 **Implementation is not included in the design.**

9. *For simplicity, you may assume there is a single system running the app (no communication or saving between devices is necessary).*

 **This makes the design simpler.**








