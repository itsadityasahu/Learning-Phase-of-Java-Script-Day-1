# Learning-Phase-of-Java-Script-Day-1
# What i am learing on Day 1 is share about below all of you see this :

📦 Day 1: Variables & Declaration

🧠 What are Variables?
Variables are containers that hold data.
They help us store, reuse, and update information in JavaScript — from simple values like
numbers to complex data like arrays and objects.
Think of a variable as a box with a name on it. You can put something inside it (a value), and later
check or change what's inside.
In JavaScript, you create these boxes using keywords: var , let , or const .

🧪 var, let, and const – Line-by-Line Comparison
🧓 var – Old and risky
Scoped to functions, not blocks
Can be redeclared and reassigned
Hoisted to the top with undefined value
js
var score = 10;
var score = 20; // OK

let – Modern and safe
Scoped to blocks ( {} )
Can be reassigned but not redeclared
Hoisted, but stays in the Temporal Dead Zone (TDZ)
js
let age = 25;
age = 30; // ✅
let age = 40; // ❌ Error (same block)

🔐 const – Constant values
Scoped to blocks
Cannot be reassigned or redeclared
Value must be assigned at declaration
TDZ applies here too
js
const PI = 3.14;
PI = 3.14159; // ❌ Error

👉 But: If const holds an object/array, you can still change its contents:
js
const student = { name: "Riya" };
student.name = "Priya"; // ✅ OK
student = {}; // ❌ Error

🔥 Scope in Real Life
Block Scope → Code inside {} like in loops, if , etc.
Function Scope → Code inside a function
let and const follow block scope.
var ignores block scope — which leads to bugs.
js
{
var x = 5;
let y = 10;
const z = 15;
}
console.log(x); // ✅ 5
console.log(y); // ❌ ReferenceError
console.log(z); // ❌ ReferenceError

🧨 Hoisting
JavaScript prepares memory before running code.
It moves all declarations to the top — this is called hoisting.
But:
var is hoisted and set to undefined
let and const are hoisted but not initialized — so accessing them early gives ReferenceError
js
console.log(a); // undefined
var a = 10;
js
console.log(b); // ❌ ReferenceError
let b = 20;

⚠️ Common Confusions (JS Reality Checks)
const doesn't make things fully constant. It protects the variable, not the value.
var is outdated — it's better to use let and const .
let and const behave similarly, but const gives more safety — use it when you're not
planning to reassign.

🧠 Mindset Rule
Use const by default. Use let only when you plan to change the value.
Avoid var — it belongs to the past.
