# Data Dictionaries

## Simple Data dictionary

Data dictionaries are used in Database Design to know what variables should be put as in a server and also include their description and name.

While being similar to the [Data Dictionaries used in Software Design](../../Year%201/Software%20Dev/Data%20Dictionaries.md) there are differences due to how we know that databases consider data e.g. using VarChar and not string.

For this example we will create a data dictionary for a cereal company where each cereal is put into a table. The data that should be saved is:

- ProductID
- Product Nae
- Product Popularity
- Target Audience
- Cost To Make
- Selling Price

A simple data dictionary would look like this:

| Variable Name | Data Type | Description |
| --- | --- | --- |
| ProductID | Integer(8) | The products ID (**Primary Key**) |
| ProductName | VarChar(127) | The name of the cereal |
| ProductPopularity | Integer(16) | Product popularity calculated by number of monthly sales |
| TargetAudience | ENUM(Kids, Teenagers, Adults) | What the target audience of the cereal is |
| CostToMake | Float | Total cost to make the cereal |
| SellingPrice | Float | Selling Price |

Some notes are that the Primary key must be included to know which one is the primary.

## More Advanced data dictionaries

A more advanced data dictionary is very similar, except there are more columns, and the names might change
As we know a database uses fields so we can change variable name to field name. field length can now also get its own row and a constraint can be added to know more about the data into it.

| Field Name | Data Type | Field Length | Constraint | Description |
| --- | --- | --- | --- | --- |
| ProductID | Integer | 8   | **Primary Key** | The products ID which auto increments sequentially |
| ProductName | VarChar | 127 | Not Null | The name of the cereal |
| ProductPopularity | Integer | 16  | Not Null | Product popularity calculated by number of monthly sales |
| TargetAudience | ENUM | 3(Kids, Teenangers, Adults) | Not Null | What the target audience of the cereal is |
| CostToMake | Float | 8   | Not Null | Total cost to make the cereal |
| SellingPrice | Float | 8   | Not Null | Selling Price |