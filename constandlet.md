# Let:
let is the variable that can be reassigned. Its use case is when you expect the value to change later.

# Example of let:
- let count: number = 5;

count = 10; // allowed
# Explanation:
- let is the variable declaration keyword in jawa and also in typescript.
- it creats a variable that can be reassigned later.
- it is blocked scope, meaning it only exist inside{} block where it is declared.

# const:
the variable cannot be reassigned.
it is use when the value stay the same.
# Example:
const pi: number = 3.14159;
// pi = 3.14;  Error: cannot reassign a const
# Explaination:
- const is used to declare variables that cannot be reassigned.

- Once you assign a value to a const, you cannot change it to something else.

- Like let, it is block-scoped.


