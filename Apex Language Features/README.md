# ApexSandbox io solutions

Duc just wants to solve some puzzles.

## Apex Language features

### sObject Type
https://www.apexsandbox.io/problem/100

Implement the method  `isTypeAccount()`, which accepts a sObject as input and returns a  `true`  if type of input is Account object else it should return as  `false`.

Given the following test code:

`Account acc = new Account(name='Apple')`

`Boolean result = isTypeAccount(acc);`

`result`  should be equal to  `true`

### Convert 15-digit ID to 18-digit ID
https://www.apexsandbox.io/problem/93

Implement the method  `convert15to18DigitId()` , which accepts a String of length 15 digit and returns a new String with 18 digit salesforce Id. If the input string length is not equal to 15 digits, then return  `'-1'`.

Given the following test code:

`String fifteenDigit = '0SO90000000PBDu';`

`String eighteenDigit = convert15to18DigitId(fifteenDigit);`

`eighteenDigit`  should be equal to  `'0SO90000000PBDuGAO'`

Note:

-   Use case 1: You have exported a Salesforce report with Ids. These Ids are 15 characters. You want to ensure that these Ids are not altered by Excel, you need to manage them with 18 characters.
-   Use case 2: You need to compare Ids but your comparison mechanism is not case sensitive. You will have to extend them to 18 characters.

### Handle Exception
https://www.apexsandbox.io/problem/97

Implement the method  `divide`  which takes two integers  `a`  and  `b`  as input, divides  `a`  by  `b`  using the  `/`  operator, and returns the result. If any exception occurs, the method should return the exception message.

Given the following test code:

`String result = divide(10,0);`

`result`  should be  `'Divide by 0';`

Given the following test code:

`String result = divide(100, 18);`

`result`  should be  `'5';`. The result of integer division  `100/19`  is  `5`  with a remainder of  `10`.

### Throw An Exception
https://www.apexsandbox.io/problem/102

Implement the method  `checkAccounts`, which accepts a list of accounts as an input and returns a list of accounts. The method should behave as follows:

-   If all accounts in the list have  `BillingCity`  present, the method should return the original list.
-   If the passed list is  `null`  the method should throw the built-in  `IllegalArgumentException`  with message  `'accounts should not be null'`
-   If any of the accounts in the list do not have a  `BillingCity`  present, the method should throw the custom  `AccountException`  exception with message  `'Invalid BillingCity'`. Do not create new exception class - use the  `AccountException`  class that has already been created for you.

Given the following test code:

`List<Account> accounts = new List<Account>();`

`accounts.add(new Account(name ='Salesforce', BillingCity ='Boston'));`

`accounts.add(new Account(name ='Microsoft'));`

The method call`checkAccounts(accounts);`  should fail, throwing an  `AccountException`.

### Safe Navigation Operator
https://www.apexsandbox.io/problem/94

Implement the method  `getAccountBillingCityWithSafeNavigation`, which accepts a list of accounts as an input and returns the  `BillingCity`  in upper case of the  **first**  account in the list. Use the Safe Navigation (?.) to ensure  `null`  is returned in case the  `BillingCity`  is null.

Given the following test code:

`List<Account> acts = new ListList<Account>();`

`acts.add(new Account(Name = 'Acme', BillingCity = 'Chicago'));`

`acts.add(new Account(Name = 'Dove', BillingCity = 'Boston'));`

`String result = getAccountBillingCityWithSafeNavigation(acts);`

`result`  should be  `'CHICAGO'`

### Dynamic Field Values
https://www.apexsandbox.io/problem/103

Implement the method  `getFieldsValue`, which accepts the following inputs:

-   An account  `acc`
-   A list of strings  `fields`, with each string in the list representing a valid field on the account object.

The method should return a list of values from the account record for fields listed in the list  `fields`  in the correct order.

Given the following test code:
```
Account acc = new Account(
    Name = 'Salesforce', 
    BillingCity = 'Boston', 
    AnnualRevenue=10000, Rating='Hot');
List fields = new List{'Industry','Name','Rating'};
List result = getFieldsValue(acc, fields);
```

`result`  should be  `[null, 'Salesforce', 'Hot']`