# Data integrity

Data integrity refers to the accuracy, consistency and completeness of the data.
Safety of data in terms of compliance with the law (e.g. GDPR)
Data integrity is important to ensure your database is efficient, preventing redundant and inaccurate data, and stopping it from being lost.
Ensuring data integrity is vital to a business, as loss of data can cause huge fines from GDPR and reputational risks (i.e. customers won't use your bank if you cannot keep your data secure)

## Entity integrity

This ensures rows are not using repeated data, and that the primary keys ensures each row is individually accessible. (Can use data types/lengths for this)
This ensures that each entity is also individually accessible

## Referential integrity

Ensures that the values between relationships are accurate (i.e. PK and FK match up), using methods like CASCADE

## Domain integrity

Ensures that each column of the entity is valid, and does not contain any duplicates or any unnecessary data.

## user-defined integrity

Ensuring that users do not implement invalid and incorrect data
This is usually done through validation and sanitation on a website or program.

# Data validation
Data validation prevents invalid or incorrect data from being inputted to the database.
This can be done through setting data types and limiting the length of the inputted value, (i.e. for a phone number, you could set it to int only and limit it to 11 digits)

There's a reason most data validation is performed outside of the database - it's very hard to set up strict rules.
However, you can at least limit the ridiculousness of some of the inputs (i.e. letters for the age, or limiting the postcode to only 7 characters)
You can also use ENUM to restrict the accepted values to only values that you allow, which is used for fields like Acess Level.

# Data security and Data control

Data contains information on the user, some of which may be sensitive and requires protection.

Examples of this might include:
- Age
- Name
- Email
- Sexual orientation
- Religious beliefs
 
## Data security techniques
- Encryption
- Restricting employee access
- Authentication
- Keeping the database up to date
- Database proxy

## Encryption
When using Encryption you should use Salts and strong, relevant encyption techniques like SHA256 over MD5
Salts are automatically generated character sets which make the passwords more secure, due to helping to hide the true password