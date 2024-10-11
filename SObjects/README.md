# ApexSandbox io solutions

Duc just wants to solve some puzzles.

## SObjects

### Duplicate Contacts
https://www.apexsandbox.io/problem/56

For this problem, we consider two Contacts as duplicates if they have the same phone number or the same email address.

Implement the method  `duplicateContacts`  that takes as input two Contact records  `c1`  and  `c1`, returns true if they are duplicates, and returns false otherwise.

For example, given the following test data:

`Contact c1 = new Contact(LastName = 'Doe', Email = 'robert@example.com');`

`Contact c2 = new Contact(LastName = 'Doe', Email = 'robert.doe@example.com');`

`duplicateContacts(c1, c2) == false`  because the two contacts do not have a phone number at all, and do not have a matching email address.

### Account Rating
https://www.apexsandbox.io/problem/57

Implement a method  `setAccountRating`  that looks at an Account's  `AnnualRevenue`, and sets the value of the  `Rating`  picklist field based on the following criteria:

-   Accounts with AnnualRevenue less than or equal to 100,000 get a rating of "Cold"
-   Accounts with AnnualRevenue less than or equal to 500,000 but greater than 100,000 get a rating of "Warm"
-   Accounts with AnnualRevenue greater than 500,000 get a rating of "Hot"

Given the following test code:

`Account a = new Account(AnnualRevenue = 150000);`

`setAccountRating(a);`

The expression  `a.Rating == 'Warm'`  should be true because the AnnualRevenue was over 100,000 but less than 500,000

### Contact Birthday
https://www.apexsandbox.io/problem/59

Given a Contact with the  `Birthdate`  field set to some date, return true if today is the Contact's birthday and return false if not. Assume that a future date will not be set on the Birthdate field.

Given the following test code:

`Contact c1 = new Contact();`

`c1.Birthdate = Date.newInstance(1992, 5, 15)`

The expression  `isBirthday(c1)`  should return true if executed on 5/15/2022 or 5/15/2020.

### Key Account
https://www.apexsandbox.io/problem/60

For this problem, we define minimum annual revenue thresholds an account must meet to be considered a key account. The annual revenue thresholds are defined by industry:

-   Banking: 600,000
-   Technology: 800,000
-   Retail: 2,000,000
-   All others: 500,000

Implement the method  `isKeyAccount`  that takes as input an Account with the  `AnnualRevenue`  field and the  `Industry`  picklist fields filled out, returns true if the account is a key account, and returns false otherwise.

`Account a1 = new Account();`

`a1.AnnualRevenue = 750000;`

`a1.Industry = 'Technology';`

The expression  `isKeyAccount(a1)`  should return false because the annual revenue does not meet the minimum threshold of 800,000 for the technology industry.

### Escalate Case
https://www.apexsandbox.io/problem/61

In-progress cases dealing with mechanical or electrical breakdown need to be escalated. Implement a method  `escalateIfMeetsCriteria`  that takes as input a Case record, and sets the  `IsEscalated`  field to true if  `Type`  is  `Mechanical`  or  `Electrical`,  `Reason`  is  `Breakdown`, and  `Status`  is  `In Progress`

Given the following test code:

`Case c = new Case();`

`c.Type = 'Mechanical';`

`c.Reason = 'Breakdown';`

`c.Status = 'In Progress';`

`escalateIfMeetsCriteria(c);`

The expression  `c.IsEscalated`  should evaluate to true because the case meets the criteria for escalations.