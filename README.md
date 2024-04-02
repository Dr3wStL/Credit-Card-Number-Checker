**README**
Credit Card Validator
This Credit Card Validator utilizes the Luhn algorithm to determine if a given credit card number is valid or invalid. It includes a set of functions designed to validate individual credit card numbers, identify invalid cards from a batch, and determine the credit card companies that have issued these invalid numbers.

**Functions**
validateCred(arr): Validates a single credit card number.
findInvalidCards(nestArr): Finds and returns all invalid credit card numbers from a nested array of card numbers.
idInvalidCardCompanies(nestArr): Identifies the companies that issued the invalid credit card numbers.

**Usage**
1. Validation of Credit Card Numbers:
The validateCred() function takes an array of digits representing a credit card number as input and returns true if the number is valid according to the Luhn algorithm, or false otherwise.

const isValid = validateCred([4, 5, 3, 9, 6, 7, 7, 9, 0, 8, 0, 1, 6, 8, 0, 8]);
console.log(isValid); // Output: true or false based on validity

2. Finding Invalid Cards:
The findInvalidCards() function takes a nested array of credit card numbers and returns a new nested array of all the invalid cards found using the Luhn algorithm.

const invalidCards = findInvalidCards(batch); // `batch` is a predefined nested array of card numbers
console.log(invalidCards);

3. Identifying Card Issuers:
The idInvalidCardCompanies() function takes a nested array of invalid card numbers and returns an array of the names of companies that have issued these invalid cards. Supported companies include Amex (American Express), Visa, Mastercard, and Discover.

const companies = idInvalidCardCompanies(invalidCards);
console.log(companies);

**Supported Credit Card Companies**
Amex (American Express): Identified by a first digit of 3.
Visa: Identified by a first digit of 4.
Mastercard: Identified by a first digit of 5.
Discover: Identified by a first digit of 6.

**Note**
The validator checks credit card numbers for validity using the Luhn algorithm but does not verify whether the card numbers are active or have been issued by the corresponding companies.

**Getting Started**
To use this validator, simply include the provided JavaScript functions in your project. Ensure you have a collection of credit card numbers to validate, represented as arrays of digits.

**Contribution**
Contributions to improve the validator or extend its functionality are welcome. Please adhere to standard coding practices and include comments where necessary.
