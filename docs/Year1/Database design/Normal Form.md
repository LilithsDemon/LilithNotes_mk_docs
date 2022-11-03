# Normal Form

### 1st Normal Form

- Add in any missing data (*if possible*)
- Identify/Create a primary key (*primary keys **must** be unique*)
    - It might be possible to make a composite key for 1NF or 2NF
    - A composite key is made up of multiple table information (*does not always work*)
    - Composite keys should only be used temporarily
- Remove duplicate information rows if they are the same
- Seperate atomic attributes
    - Atomic attributes are attributes that can be futher split up
        - E.G. a full name can be split into a first and second name

For example we will use this table as an example:

| Employee Name | Salary | Job Title | Project | Project Start Date | Project End Date | Manager |
| --- | --- | --- | --- | --- | --- | --- |
| Sam Smith | 26000 | Rookie | Bravo | 01/02/2022 | 01/02/2023 | Lt Alex Jones |
| Mick Mann | 33000 |     | Charlie | 02/01/2021 | 02/01/2024 | Lt Alex Jones |
|     | 33000 | Corporal |     |     | 02/01/2024 |     |
| Adam Artic | 40000 | Sergeant | Alpha | 03/04/2016 | 04/03/2029 | Cl Jess Hawke |
| Sam Smith |     | Rookie |     | 01/02/2022 |     |     |

As you can tell by this table there is a lot of duplicate and missing data in the table, our first thing to do would be to ensure any missing data is filled.
In this case some data can be moved across to different rows before deleting duplicate rows to ensure that all the data is correct.

For example from row 2 we know that Mick Mann has a salary of 33000 and then by comparing with row 4 he is a corporal as data is the same in each.
We can then get rid of duplicate rows such as the third row and we can see the 5th row is the same as the first row.

Therefore this is what our table would look like in 1NF:

| Composite key | First Name | Last Name | Salary | Job Title | Project | Project Start Date | Project End Date | Manager |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Rookie Sam Smith | Sam | Smith | 26000 | Rookie | Bravo | 01/02/2022 | 01/02/2023 | Lt Alex Jones |
| Corporal Mick Mann | Mick | Mann | 33000 | Corporal | Charlie | 02/01/2021 | 02/01/2024 | Lt Alex Jones |
| Sergeant Adam Artic | Adam | Artic | 40000 | Sergeant | Alpha | 03/04/2016 | 04/03/2029 | Cl Jess Hawke |

* * *

### 2nd Normal Form

- First Check that data is in 1NF
- Remove any partial dependancies
    - A partial dependancy is where one or more of the attributes depends on part of the primary key
    - This can occur if the primary key is a composite key
- Fix any many-to-many relationships
    - *A database cannot have many to many relationships*
        - *If there is a many to many realtionship it shoud be changed to a one-to-many then a many-to-one table*

So for out 2nd Normal form we would split this into multiple different tables that all link with each other

| Employee ID | First Name | Last Name | Job Title | Project |
| --- | --- | --- | --- | --- |
| 1   | Sam | Smith | Rookie | Bravo |
| 2   | Mick | Mann | Corporal | Charlie |
| 3   | Adam | Artic | Sergeant | Alpha |

| Job Title | Salary |
| --- | --- |
| Rookie | 26000 |
| Corporal | 33000 |
| Sergeant | 40000 |

| Project | Project Start Date | Project End Date | Manager |
| --- | --- | --- | --- |
| Alpha | 03/04/2016 | 04/03/2029 | Cl Jess Hawke |
| Bravo | 01/02/2022 | 01/02/2023 | Lt Alex Jones |
| Charlie | 02/01/2021 | 02/01/2024 | Lt Alex Jones |

This is now second normal form as there is now not a composite key and there is not a many to many realtionship

* * *

### 3rd Normal Form

- First check that data is already in 2NF
- Check there are no "key dependancies"
    - A non-key dependancy exists where the value of an attribute is determined by a factor that is not part of a key
- In this example we can tell that the manager is not fully dependant on the Project and can be different therefore Manager can be a table

| Employee ID | First Name | Last Name | Job Title | Project |
| --- | --- | --- | --- | --- |
| 1   | Sam | Smith | Rookie | Bravo |
| 2   | Mick | Mann | Corporal | Charlie |
| 3   | Adam | Artic | Sergeant | Alpha |

| Job Title | Salary |
| --- | --- |
| Rookie | 26000 |
| Corporal | 33000 |
| Sergeant | 40000 |

| Project | Project Start Date | Project End Date | Manager |
| --- | --- | --- | --- |
| Alpha | 03/04/2016 | 04/03/2029 | 2   |
| Bravo | 01/02/2022 | 01/02/2023 | 1   |
| Charlie | 02/01/2021 | 02/01/2024 | 1   |

| Manager ID | Manager |
| --- | --- |
| 1   | Lt Alex Jones |
| 2   | Cl Jess Hawke |