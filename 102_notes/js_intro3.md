# Comparison and logical operators & FOR and WHILE Loops

## Comparison and logical operators

### Comparison operators

You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a Boolean: **true** or **false**.

1. == 
    - is equal to 
    - this operator compares 2 values to see if they are the same
2. === 
    - strict equal to 
    - this operator compares two values to check that both the data type and value are the same.
3. !=
    - is not equal to
    - this operator compares 2 values to see if they are _not_ the same.
4. !==
    - strict not equal to
    - this operator compares 2 values to check that both he data type and value are _not_ the same.
5. `>`
    - greater than
6. < 
    - less than 
7. `>`=
    - greater than or equal to
8. <=
    - less than or equal to 

### Logical operators 

Comparison operators usually return single values of **true** or **false**. Logical operators allow you to compare the results of more than one comparison operator.

```javascript
((5 < 2) && (2 >= 3))
```

1. && 
    - LOGICAL _**AND**_
    - if both expressions evaluate to **true** then the expression returns **true**. If just one of these returns **false**, the the expression will return **false**.
2. ||
    - LOGICAL _**OR**_
    - if either expression evaluates to **true**, then the expression returns **true**. If both return **false**, then the expression will return **false**.
3. !
    - LOGICAL _**NOT**_
    - this reverses the state of an expression. If it was **false** it would return **true**. If the statement was **true**. it would return **false**
> !true returns false; !false returns true;


## Loops 

Loops check a condition. If it returns **true**, a code block will run. Then the condition will be checked again and if it still returns **true**, the code block will run again. It repeats until the condition returns **false**. There are three common types of Loops:

### **FOR LOOPS**
    - If you need to run code a specific number of times, use a for loop. In a for loop, the condition is usually a counter which is used to tell how many times the loop should run.

```javascript
for (var i = 0; i < 10; i++) {
    document.write(i);
    
}
``` 


### **WHILE LOOPS**
    - The purpose of a while loop is to execute a statement or code block repeatedly as long as an expression is true. Once the expression becomes false, the loop terminates.

```javascript
var count = 0;
 document.write("Starting Loop ");
         
while (count < 10) {
    document.write("Current Count : " + count + "<br />");
    count++;
}
``` 


[<== Back to ReadMe](../README.md)
