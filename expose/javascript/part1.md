1. Line 9 will print "values added: 20"
2. Line 13 will print "final result: 20"
3. Line 9 will print "values added: 20"
4. Line 13 will have a reference error because result was created with the `let` keyword which has block scope so after the if statement scope, it doesn't know the value of result anymore.
5. Line 9 will throw an error because in line 5, result was already declared with the `const` keyword with a value of 0. Then we are trying to change the value of a const by doing `result = num1 + num2;` which we are not allowed to do.
6. Line 13 will throw an error, but for a different reason than number 5. Const is block scoped meaning that the compiler wouldn't know the value of result after the if statement scope meaning it would throw a reference error.  