# Data type in typescript:
  # define:
     In TypeScript, a data type is a label that tells the compiler what kind of value a variable,
     function parameter, or return value can hold.
     It defines the shape and kind of data so TypeScript can check correctness before running the code.
  # Example:
  let age: number = 20;       // must be a number
 
  let name: string = "Ali";   // must be text
  # Categories:
- Primitive types
- Objective types
- Special types
- Adwanced types
- Function types
  #  1  Permitive type:
- Number
- string
- Bolean
- Null
- Undefined
- Bigint
- Symbol
- # Example:
  let username: string = "Ali";       // text
   
  let age: number = 20;              //number

  let isStudent: boolean = true;      // true/falses
  # 2 Objective type:
  - Array
  - Tuple
  - Object
  # Example:
  let age: number = 25;

let name: text = "Ali";

let isDone: Boolean = true;
# 3 Special data types
- Any
- Unknown
- Void
- Never
# Example:
- // 1) any — disables type checking (use carefully)
let data: any = 5;
data = "Hello"; // allowed
data = true;    // allowed


- // 2) unknown — type-safe "any"
let value: unknown = "Hello";
if (typeof value === "string") {
  console.log(value.toUpperCase()); // must check type before use
}


- // 3) void — no return value
function logMessage(message: string): void {
  console.log(message);
}


- // 4) never — function never finishes normally
function throwError(msg: string): never {
  throw new Error(msg);
}
# 4 Advanced type
- Union
- intersection
- Type Alias
- Enum
- Literal types
# Example:
- // 1) Union type — value can be one of several types
let id: string | number;
id = "abc123";
id = 101;

- // 2) Intersection type — combine multiple types
type Person = { name: string };
type Employee = { employeeId: number };
type Staff = Person & Employee;
const staffMember: Staff = { name: "Ali", employeeId: 42 };

- - // 3) Generics — reusable types
function wrap<T>(value: T): { item: T } {
  return { item: value };
}
const wrappedNumber = wrap(123);      // T = number
const wrappedString = wrap("hello");  // T = string

- // 4) Utility types — built-in helpers
interface User {
  id: number;
  name: string;
  email?: string;
}
type UserPreview = Pick<User, "id" | "name">; // pick some properties
const user: UserPreview = { id: 1, name: "Aisha" };

- // 5) Conditional types
type IsString<T> = T extends string ? "yes" : "no";
type Test1 = IsString<string>; // "yes"
type Test2 = IsString<number>; // "no"
# 5 Function types
- defines the type of function
# Example:
- // 1) Simple function type
function add(a: number, b: number): number {
  return a + b;
}

- // 2) Function type as a variable
let greet: (name: string) => string;
greet = function (name) {
  return `Hello, ${name}`;
};

- // 3) Function type with type alias
type MathOperation = (x: number, y: number) => number;
const multiply: MathOperation = (x, y) => x * y;

- // 4) Optional and default parameters
function log(message: string, userId?: number): void {
  console.log(message, userId ?? "Guest");
}
function power(base: number, exponent: number = 2): number {
  return base ** exponent;
}

- // 5) Generic function type
function identity<T>(value: T): T {
  return value;
}
let num = identity<number>(42);
let str = identity("TypeScript");


  
