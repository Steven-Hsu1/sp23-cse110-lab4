1. The value of **i** at that point would be **3** because the for loop would run until `i < prices.length` and would become 3 before that statement becomes false. Since this was declared using a `var` keyword, it is function scoped meaning **i** can be accessed outside the for loop with it's updated value being **3**.
2. This would print out a value of **150** for `discountedPrice` because it was delcared using the `var` keyword which has function scope meaning it is accessible outside the for loop. Since the last iteration of the loop runs with `i = 2`, we would get `prices[2] * (1 - 0.5)` which would lead to **150**.
3. This would lead to the output **150** because like in the previous questions, `var` is function scoped and `finalPrice` was declared with that keyword meaning it can be seen throughout the entire function. Then taking our answer from #2, `Math.round(150 * 100) / 100` would return **150** as there is nothing to round.
4. This function would return **[50, 100, 150]** because the for loop iterates and essentially multiplies each element of `prices` by 0.5 and then it is pushed back onto another array called `discounted` and since discounted is declared with `var`, it exists the entire time of the function's runtime.
5. At line 12, the code will cause a **Reference Error** because **i** was declared with `let` which is block scoped meaning it cannot be seen outside the for loop which is where the `console.log` is located.
6. At line 13, the code will cause a **Reference Error** because `discountedPrices` was declared with `let` inside of the for loop meaning it can only be seen within that scope. We cannot access it anymore by the time we reach the `console.log`.
7. This would print out **150** because `finalPrice` was declared with `let` but it exists within the block of the function. This means that anything inside of the function `discountPrices` can see this variable and use it, so it would lead to the same outcome as #3 which was **150**.
8. This function would return **[50, 100, 150]** because `discounted` was declared with `let` within the entire function block meaning that it can be accessed by the for loop and after, leading to similar reasoning as #4.
9. At line 11, this would throw a **Reference Error** because **i** is declared with the block scoped `let` within the for loop so `console.log(i)` doesn't know what i is anymore.
10. This would print **3** because we declared `length` as a `const` but it's block scope encapsulates all of the function meaning that the `console.log` can access the length of prices which has 3 elements within it.
11. This would print out **[50, 100, 150]** because although it would seem like we are redeclaring `const discountedPrices = prices[i] * (1 - discount)`, since the const is declared within the for loop block, each time a new iteration happens, it's like redeclaring it inside of a new block which is ok to do with const, just not within the same block. Then it just applies the 50% discount and pushes it onto the `discounted` array. Another thing to note is that although we are changing the array that `discounted` points to, we are not actually changing the reference which is what const cares about. This is why we want to usually use const for declaring objects and such.
12. Answers
    1.  student.name
    2.  student['Grad Year']
    3.  student.greeting()
    4.  student['Favorite Teacher'].name
    5.  student.courseload[0]
13. Answers
    1.  **'32'** because sees the string '3' and so converts the 2 to a string as well to concatenate it.
    2.  **1** because there is no subtraction with strings so it converts '3' into a number to subtract from 2. This is why the final answer is also of type `number`.
    3.  **3** because it sees 3 as a number then null is also 0 so 3 + 0 = 3.
    4.  **'3null'** because it sees '3' as a string and so converts null into a string as well to concatenate.
    5.  **4** because true is converted to 1 and added to 3.
    6.  **0** because false is converted to an int as well as null because that is a common type between the two resulting in 0.
    7.  **'3undefined'** because it converts undefined into a string to concatenate.
    8.  **NaN** because undefined cannot be converted to a number so it becomes NaN which stands for Not a Number so when subtracting from that, it stays not a number.
14. Answer
    1.  **true** because '2' is converted into a number and it is indeed greater than 1 so it returns true.
    2.  **false** because string comparisons happen character by character so it sees 2 < 1 which is false
    3.  **true** because '2' is converted into a number so 2 == 2.
    4.  **false** because the triple equals requires both sides to be of the same type to even consider if they are equal.
    5.  **false** because true would turn into the number 1 which is not equal to 2.
    6.  **true** because Boolean(2) is evaluated to be true and true is the same as true.
15. The `==` operator is a loose equality operator while `===` is a strict equality operator. Basically a loose equality operator will still return true if javascript can convert the type to match vs. a strict equality operator, the two sides must have the same type without any javascript casting.
<!-- 16.  -->
17. The result of the call to `modifyArray` would be **[2, 4, 6]** because we are passed in an array and a modifying function. We loop through the length of the array which happens to be of length 3 and then the callback function takes in a number input and multiplies it by 2. So each iteration of the loop, array[i] would be mutliplied by 2 and added to the new array. Then this is essentially just doubling each element in the original array and returning it.
<!-- 18.  -->
19. 1 -> 4 -> 3 -> 2 because the setTimeout creates an async environment so the call stack of the runtime needs to be popped off first before the new stack of the setTimeout can be executed. This is why even though there is a 0 ms delay timeout, it still goes after all non-callback runtime executions.