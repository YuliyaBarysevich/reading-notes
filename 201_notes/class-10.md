# JavaScript Debugging

If a JavaScript statement generates an error, then it throws an exception . At that point, the interpreter stops and looks for exception-handling code.

## ERROR OBJECTS

Error objects can help you find where your mistakes are and browsers have tools to help you read them.  

There are seven types of built-in error objects in JavaScript.

1. **Error**
    - Generic error - the other errors are all based upon thes error
2. **SyntaxErroe**
    - Syntax has not been followed
    - MISMATCHING OR UNCLOSED QUOTES (`SyntaxError: Unexpect ed EOF`)
    - MISSING CLOSING BRACKET (`SyntaxErr or : Expected token ')'`)
    - MISSING COMMA IN ARRAY
3. **ReferenceError**
    - Tried to reference a variable that is not declared/whithin scope
    - VARIABLE DOES NOT EXIST
    - VARIABLE IS UNDECLARED (`ReferenceError: Can't find variable: height`)
    - NAMED FUNCTION IS UNDEFINED(`ReferenceError: Can't find variable: randomFunction`)
4. **TypeError**
    - An unexpected data type that cannot be read 
    - VALUE IS UNEXPECTED DATA TYPE (`TypeError: 'undefined' is not a function (evaluating 'Document.write('Oops! ')')`)
    - INCORRECT CASE FOR write() METHOD (`TypeError: 'undefined' is not a function (evaluating 'document.Write('Oops!')')`)
    - METHOD DOES NOT EXIST (`TypeError: 'undefined ' is not a function (evaluating 'box.getArea()')`)
    - DOM NODE DOES NOT EXIST (`TypeError: 'null' is not an object (evaluating 'el .innerHTML = 'Mango'')`)
5. **RangeError**
    - Numbers not in acceptable range
    - NUMBER OUTSIDE OF RANGE (`RangeError: Array size is not a small enough positive integer`)
    - NUMBER OF DIGITS AFTER DECIMAL IN tofhed() CAN ONLY BE 0-20 (`RangeError: toFixed() argument must be between 0 and 20`)
6. **URIError**
    - encodeURI ().decodeURI(),and similar methods used incorrectly
7. **EvalError**
    - eval() function used incorrectly
8. **NaN**
    - If you perform a mathematica l operation using a value that is not a number, you end up with the value of NaN, not a type error.  

## Debugging Workflow 

1. WHERE IS THE PROBLEM?

First, should try to can narrow down the area where the problem seems to be. In a long script, this is especially important.  

  Look at the error message, it tells you:
- The relevant script that caused the problem.
- The line number where it became a problem for
the interpreter. (As you will see, the cause of the error may be earlier in a script; but this is the point at which the script could not continue.)
- The type of error (although the underlying cause of the error may be different).

2. WHAT EXACTLY IS THE PROBLEM?

Once you think that you might know the rough area in which your problem is located, you can then try to find the actual line of code that is causing the error.

  Break down I break out parts of the code to test smaller pieces of the functionality.
- Write values of variables into the console.
- Call functions from the console to check if they are returning what you would expect them to.
- Check if objects exist and have the methods I
properties that you think they do.  

## Debugging Tips 

- ANOTHER BROWSER
    - Some problems are browser- specific. Try the code in another browser to see which ones are causing a problem.
- ADD NUMBERS
    - Write numbers to the console so you can see which the items get logged. It shows how far your code runs before errors stop it.
- STRIP IT BACK
    - Remove parts of code, and strip it down to the minimum you need. You can do this either by removing the code altogether, or by just commenting it out.
- EXPLAINING THE CODE
- SEARCH
    - Stack Overflow is a Q+A site for programmers.


## COMMON ERRORS

1. GO BACK TO BASICS
    - JavaScript is case sensitive so check capitalization.
    - If you did not use var to declare the variable, it will be a global variable, and its value could be overwritten elsewhere (either in your script or by another script that is included in the page).
    - If you cannot access a variable's value, check if it is out of scope (declared within a function that you are not within).
    - Do not use reserved words or dashes in variable names.
    - Check that your single I double quotes match properly.
    - Check that you have escaped quotes in variable values.
    - Check in the HTML that values of your id attributes are unique.
2. MISSED/ EXTRA CHARACTERS
    - Check that there are no missing closing braces } or parentheses )
    - Check that there are no commas inside a , } or ,) by accident.
    - Always use parentheses to surround a condition that you are testing.
    - Check the script is not missing a parameter when calling a function.
    - undefined is not the same as nu11 : nu11 is for objects, undefi ned is for properties, methods, or variables.
    - Check that your script has loaded (especially CDN files).
    - Look for conflicts between different script files.
3. DATA TYPE ISSUES
    - Using= rather than == will assign a value to a variable, not check that the values match.
    - If you are checking whether values match, try to use strict comparison to check datatypes at the same time. (Use === rather than ==.)
    - Inside a switch statement. the values are not loosely typed (so their type will not be coerced).
    - Once there is a match in a switch statement, all expressions will be executed until the next br eak or return statement is executed.
    - If you are using the parseInt() method, you might need to pass a radix (the number of unique digits including zero used to represent the number).



  
[<== Back to ReadMe](../README.md)
