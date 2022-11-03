# Pseudocode

Pseudocode is code that is written in the english langauge using easy to read notation that does not follow many syntax rules as usual programming langauges.
This allows programs to be *easier* to code.

Pseudocode is used to to help plan out an algorithm/program in plain English, this means it can be understood regardless of what langauge it is intended to be built in.

This helps with reusability, as we can easily understand Pseudocode, whereas we may not understand the algorithm when built in a langauge we do not recognise

Pseudocode also helps plan out the program developement, as we can map out how we want the program to function before we develop it.

This can help show project stakeholders how the intended solution will work.

## Pseudocode rules

- One Statement per line
- Capitalised Key words
- Use indentation to use hierarchy
- Use and END statement to symbolise the end of a multi-line structure
- Keep your statements in English, minimise syntax

## Pseudocode Syntax

### Input and output

To get input you use INPUT such as:
`Input first name AS varFirstName`
To output you would use OUTPUT such as:
`OUTPUT varFirstName`

### Control Statements

#### If statements

For If statements as said earlier we have to use ENDIF at the end and use caps
For example

```
IF Age >= 10 THEN
        SET status to "Child"
ELSE IF Age == 20 THEN
        SET status to "Adult"
ELSE THEN
        SET status to "unsure"
ENDIF	
```

#### Switch Case

Switch work similar to standard c++ but written a little nicer and can be used in one statement For example

```
CASE OF Answer
        'A': OUTPUT "Wrong"
        'B': OUTPUT "Correct"
        'C': OUTPUT "Wrong"
        'D': OUTPUT "Wrong"
        OTHER: OUTPUT "Invalid Option"
ENDCASE
```

### Iteration Statements

There are many forms of iteration through pseudocode
These are examples are here:

```
/* Do Statement */
DO
        Age = Age + 1
UNTIL Age >= 15

/* DO WHILE statement */
DO WHILE Age <= 15
        Age = Age + 1
END WHILE

/* FOR loop */
FOR A IN 1 To 5
        OUTPUT A
END FOR
```

### Functions and Procedures

When using functions and procedures it could be useful to include the main, this is the bit of a program that is ran when the code starts, it should be after all the functions and procedures it relies on as it cannot call funtions and procedures after it as they would not have been compiled or interpreted.

To show what the main part of a program is we would use:

```
PROGRAM START (MAIN)
    INPUT Number1
    OUTPUT Number1
END PROGRAM
```

And then for functions and procedures we will just use FUNCTION and PROCUDURE and then the END versions of them.

If you are giving parameters to a function or procedure you must first include "PASS VARIABLES" before the paramters to show that they are being passed.

For example:

```
PROCEDURE outputNums(PASS VARIABLES num1, num2, num3)
        OUTPUT "First Number: " + num1
        OUTPUT "Second Number: " + num2
        OUTPUT "SUM: " + num3
ENDPROCEDURE
```

```
FUNCTION sumNums(PASS VARIABLES num1, num2)
        varNums = num1 + num2
        RETURN varNUMS
ENDFUNCTION
```

## Examples of code

### Multiplication of 2 numbers Example
An For this pseudocode we should:
- Input 2 numbers
- Mulitply the 2 numbers together
- Output the number

This would look like this:
```
OUTPUT "Enter number 1"
INPUT first number AS varNum1
OUTPUT "Enter number 2"
INPUT second number AS varNum2

OUPUT varNum1 multiplied by varNum2
```

### Check if input is a specific value
In this example we should:
- Takes a users number input
- Output to tell the user if their value is not a 5 or a 6

This would look like:
```
OUTPUT "Enter a number: "
INPUT number AS varNumber
IF varNumber is NOT equal to 5 OR varNumber is NOT equal to 6
    OUTPUT "That number is not a 5 or a 6"
ENDIF
```

### Colour selecter
This code example will:
- Ask a user to enter a number
    - If the number is between 0 and 10
        - Write Blue
    - If the number is between 10 and 20
        - Write the word Red
    - If the number is between 20 and 30
        - Write the word Green
    - If there is another number
        - Write that it is not a correct colour option

```
OUTPUT "Please enter a number: "
INPUT number AS varNumber
IF varNumber >= 0 AND varNumber < 10
        SET varOutput AS "Blue"
ELSE IF varNumber >= 10 AND varNumber < 20
        SET varOutput AS "Red"
ELSE IF varNumber >= than 20 AND <= 30
        SET varOutput AS "Green"
ELSE
        SET varOutput AS "That is not a correct colour option"
ENDIF
        
OUTPUT varOutput
```

### Multiples of 5 between 1 and 100
So for this example we will make pseudocode that will print all multiples of 5 between 1 and 100 (including both 1 and 100) *** using MOD ***

```
SET varNum AS 1
DO
    varNum is equal to varNum + 1
    IF varNum MOD 5 is equal to 0
            OUPTUT varNum
    ENDIF
UNTIL varNum is equal to 101

/*
Note -->
There are multiple ways to do this for example with a While or a for loop
Or if you did not have to use MOD you could just keep adding up in 5s
However using MOD this is 1 of the many ways you can do this
*/
```

### Count multiples of 2

In this example we will count all even numbers up to a user defined stopping point
The code should use either a function or procedure to gather the user input, and to count and output all the even numbers

```
FUNCTION getNumber()
        OUTPUT "Please enter a stopping point: "
        INPUT number AS varStopPoint
        RETURN number
ENDFUNCTION

PROCEDURE outputEvenNumbers()
        FOR i IN 2 to varStopPoint
                IF i MOD 2 == 0
                        OUTPUT i
                ENDIF
ENDPROCEDURE

PROGRAM START (MAIN)
        SET varStopPoint AS CALL getNumber()
        CALL outputEvenNumbers(varStopPoint)
ENDPROGRAM
```