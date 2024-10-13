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

### Same Parent
https://www.apexsandbox.io/problem/63

Implement the method  `sameParent`  that takes as input an opportunity  `opp`  and a contact  `c`, and returns true if both the opportunity and contact have the same parent account.

Given the following test code:

`Contact con = new Contact(AccountId = '0018c00002CQU9EAAX');`

`Opportunity opp = new Opportunity(AccountId = '0018c00002CQU9EAAX');`

The method call  `sameParent(con, opp)`  returns true because both the contact and the opportunity have the same parent account.

### Same Parent II
https://www.apexsandbox.io/problem/64

Implement the method  `sameParent`  that takes as input an account  `acc`, a contact  `con`, and an opportunity  `opp`  and returns true if both the opportunity and contact have the given account as the parent.

Given the following test code:

`Account acc = new Account(Id = '0018c00002CQU9EAAX');`

`Contact con = new Contact(AccountId = acc.Id);`

`Opportunity opp = new Opportunity(AccountId = acc.Id);`

The method call  `sameParent(acc, con, opp)`  returns true because both the contact and the opportunity have the same parent account.

### Set Parent Account
https://www.apexsandbox.io/problem/66

Implement the method  `setParent`  that takes as input an account  `acc`, a contact  `con`, and an opportunity  `opp`  and sets the account is the parent for both the opportunity and contact. Make sure to not take any action if the provided account or its Id is null.

Given the following test code:

`Account acc = new Account(Id = '0018c00002CQU9EAAX');`

`Contact con = new Contact(LastName = 'Smith');`

`Opportunity opp = new Opportunity(Name = 'Coding Bootcamp');`

`setParent(acc, con, opp);`

The expression  `opp.AccountId == '0018c00002CQU9EAAX' && con.AccountId == '0018c00002CQU9EAAX'`  returns true because both the contact and the opportunity now have  `acc`  as the parent account.

### Set Parent Case
https://www.apexsandbox.io/problem/67

Implement the method  `linkParent`  that takes as input two cases  `c1`  and  `c2`, and sets the case created first as the parent of the case created later  _only if_  both cases look up to the same Contact. Ensure to handle the special case where the cases do not have any related contacts.

Given the following two cases:

`**c1**`

`Id: '5008c00001GHfeUAAT'`

`CreatedDate: 2022-01-17 05:15pm GMT`

`ContactId: '0035f00000A4REqAAN'`

`Subject: 'Not able to log in'`

`**c2**`

`Id: '5008c00001GHfeoAAD'`

`CreatedDate: 2022-01-19 2:34pm GMT`

`ContactId: '0035f00000A4REqAAN'`

`Subject: 'User not created in system of record'`

and given the following test code:

`linkParent(c1, c2);`

The case  `c1`  should be set as the parent of case  `c2`  since they are both related to the same Contact and  `c2`  was created after  `c1`.