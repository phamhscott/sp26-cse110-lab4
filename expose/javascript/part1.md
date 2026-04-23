1. "values added: 20" is printed by line 9.

2. "final result: 20" is printed by line 13. This is because of the use of "var" which makes the result variable have function scope.

3. var should not be used because these type of variables ignore block scopes which can lead to misuse or unintended use of these variables as they can have bigger scopes and exist when they shouldn't (leading to bugs/errors). Furthermore, var allows declaration of same variable name multiple times in the same scope without giving an error which can lead to more bugs.

4.  "values added: 20" is printed by line 9.

5.  The code returns an error (ReferenceError) when trying to print line 13. This is because the result variable is declared using the let keyword inside the if statement block. "let" variables are block-scoped, so they only exist within the blocks they are defined. Hence when line 13, which exists outside of the result variable's scope tries to print it, it is no longer defined and causes to code to return an error.

6. The code will return an error (TypeError) and not print line 9. This is because of the variable result is defined as a "const," which means it can't be reassigned. On line 7, when result tries to be reassigned to a new value, this is therefore not allowed and what causes the program to crash.

7. Similarly, the code will return an error and not print line 13. Result is defined with the "const" keyword which means it can't be reassigned and also is block-scoped (same scope as "let"). On line 7, we see result trying to be reassigned, which is no allowed, but regardless since result is defined within the if statement block, line 13 wouldn't even be able to access result because it is outside of the block.

