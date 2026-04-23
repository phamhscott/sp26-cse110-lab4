1. The bug is string concatenation. num1 and num2 is defined by document.getElementByID().value which returns a string. So when result is defined as num1 + num2, the + operator perform concatenation of two strings. So if num1 was '1' and num2 was '2' for example, the result would be '12' rather than the mathematical/numerical addition of 1 + 2 = 3.

2. To fix this I would convert the string values to numbers using Number() either before or during the calculation.
   [fix.png](../../expand/screenshots/fix.png)