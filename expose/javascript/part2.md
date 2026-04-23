1. Line 12 will cause the program to print "3." This is because i is declared with the keyword "var." Variables declared with "var" have function scope which means that i is accessible anywhere in this discountPrices function, even after the for loop finished. As the input prices array has a length of 3, on termination of the for loop, i will be set to 3. Therefore when the program reaches line 12, it will print the length of the prices array, which is 3.

2. Line 13 will cause the value "150" to be printed out to console. For a similar reason, discountedPrice is a variable declared using the "var" keyword. This means it has function scope and so anywhere in the discountPrices function can access this variable, even after the for loop terminates. As the for loop iterates across the length of the prices array (which is 3), on the last iteration it will take element 300 (element 3 of array) and multiply this by (1 - 0.5) (0.5 is discount) which has the value of 150. When the program reaches line 13, it will print out this value since it still has access to the discountedPrice variable.

3. Line 14 will cause the console the print out "150." For a similar reason, since finalPrice is declared using the "var" keyword it has function scope and so anywhere in the function can access this variable, even after the for loop terminates. On the last iteration of the for loop, finalPrice receives its last change, taking discountedPrice, which is 150, and running the math round operation one finalPrice *100 / 100. This evaluates to 150 and so line 14, which still has access to finalPrice, will print out 150 as a result.

4. The function will return the array [50, 100, 150]. The variable discounted is declared using the "var" keyword so it has function scope and can be accessed anywhere in the function. On every iteration of the for loop, the finalPrice value is pushed to this array. We can calculate this finalPrice value across each of the 3 iterations (as prices array has length 3). The first is 50 (following the input price 100), then 100 (input price is 200), and lastly 150 (input price is 300). Therefore when we push these values when iterating across the for loop we will end up with [50, 100, 150] when the for loop terminates, for the function to return in the end.

5. The code will cause an error (ReferenceError) when trying to execute line 12. This is because the i variable which the program tries to print to console is declared using the "let" keyword. "let" variables are block-scoped, so they only exist within the blocks they are defined. Since the i variable is declared inside the for loop block, when line 12, which exists outside of the i variable scope," tries to print it, it is no longer defined and causes to code to return an error.

6. The code will cause an error (ReferenceError) when trying to execute line 13. This is because the discountedPrice variable is declared using the let keyword which means it has block scope. The variable discountedPrice is declared inside the for loop block, so when line 13, which is outside of this block, tries to access this variable, it is no longer defined and causes to code to return an error.

7. At line 14, the code will print out the number "150" to console. Firstly, even though the finalPrice variable is declared with the "let" keyword, it is declared at line 4 which is outside of the for loop block. So anywhere in this function an access this finalPrice variable. finalPrice holds the last finalPrice value of the for loop, which is when the input price is 300, so its value is 150. So one line 14, which has access to this variable, it will print out 150.

8. For a similar reason as above, the function will return the array [50, 100, 150]. The variable discounted is declared with the "let" keyword however it is declared on line 4, outside of the for loop block, and so anywhere in the function has access to this variable. As we saw previously discounted is an array with the pushed finalPrices of each iteration. Thus when the for loop terminates it has the pushed values 50, 100, and 150 (from input 100, 200, and 300 respectively). The function then returns this array which it still has access to.

9. The code will cause an error (ReferenceError) when trying to execute line 11. The variable i is declared with the "let" keyword inside of the for loop block. "let" variables are block-scoped and so when line 11, which is outside of the i variable scope tries to access it to print out to console, it cannot access it and thus the code will return an error.

10. The code will print out the value "3" to console. One line 4, the length variable is declared using the "const" keyword which means it can't be reassigned. The variable length never is reassigned, so there is no error that will be caused there. Furthermore it has block scope (similar to "let") and declared outside of the for loop which means anywhere in the function has access to it. Since the input array has length 3, on line 12, when it prints out length, it will print out 3.

11. The function will return the array "[50, 100, 150]". The discounted variable is a "const" variable so it can't be reassigned and has block scope. Since it is declared outside of the for loop, anywhere int he function can access it. We see that in the for loop, discounted gets pushed the discountedPrice value of each price (100, 200, 300) with discount 0.5. Even though the variable can't be reassigned, it is still mutable, so push operations will not cause an error. Therefore when the for loop terminates, discounted will be the array of pushed values "[50, 100, 150]," the discounted prices, and when line 14 runs to return it, it can because it still has access to the variable.

12.

- A. ```student.name```
- B. ```student['Grad Year']```
- C. ```student.greeting()```
- D. ```student.['Favorite Teacher'].name```
- E. ```student.courseLoad[0]```

13.

- A. Output: '32'. The + operator triggers string concatenation if one operand is a string.
- B. Output: 1. The - operator only works with numbers, so the string '3' is mapped to number 3.
- C. Output: 3. For numeric addition, null is mapped to 0.
- D. Output: '3null'. One operand is a string, so null is mapped to 'null' and concatenated.
- E. Output: 4. In numeric contexts, boolean if mapped to 1.
- F. Output: 0. Both operands are mapped to numbers with false -> 0 and null -> 0.
- G. Output: '3undefined'. The + operator triggers string concatenation so undefined is mapped to 'undefined'.
- H. Output: NaN. The - operator converts operands to numbers. undefined becomes NaN and any operation with NaN results in NaN.


14.

- A. Output: true. When comparing a string and a number, the string '2' is mapped to number 2.
- B. Output: false. When comparing two strings, the comparisons are done in lexicographical order and '2' comes after '1'.
- C. Output: true. The loose equality operator converts the string '2' to number 2.
- D. Output: false. The strict equality operator checks both value and type and one value is a string and the other a number.
- E. Output: false. Both are converted to numbers so true becomes 1.
- F. Output: true. Boolean(2) converts 2 to true and now both sides have boolean true.

15. == is loose equality which compares two values for equality after converting both to a common type. On the other hand === is strict equality and compares both the value and data type. No immediate type mapping occurs and if the types are different, the result is false.

16. [part2-question16.js](./part2-question16.js)

17. At the end of the function, newArr will be equal to [2,4,6] which it will return. On line 13, when the modifyArray function is called, it has the arguments [1,2,3] as well as the function doSomething. Inside the modifyArray function, we first initialize a newArr variable. Then we have a for loop which iterates over the length of the input array (length 3), in which each iteration pushed the result of the doSomething function (callback input function) when its input is the array element being indexed currently. The doSomething function multiples the input value by 2. Thus each iteration of the for loop essentially takes the value of the input array, multiplies it by 2, and pushed it into newArr. Thus it does so for each value [1,2,3]of the input array, and so the pushed values would be [2,4,6] which the modifyArray function returns in the end.

18. [part2-question18.js](./part2-question18.js)

19. Output:
    ```
    1
    4
    3
    2
    ```