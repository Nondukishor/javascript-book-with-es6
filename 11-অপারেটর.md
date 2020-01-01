<h1 align="center"> অপারেটর </h1>
অপারেটর মানে হলো যে অপারেশন করে মানে যে কাজ অপারেট করে থাকে । আমরা গনিতে যে অপারেটর গুলো নিয়ে পড়ালেখা করে এসেছি সেগুলোই আবার এইখানে ব্যবহার করব তাই এইখানে তেমন কঠিন কিছু নাই । অনেকেই অনেক ভাবে বলে আমি যেভাবে অপারেটর কে সংজ্ঞায়িত করে থাকি তা হলো অপারেটর হলো ঘটক এর মতো যে বর কনে এর মাঝে সম্পর্ক স্থাপন করে দেয় । সুতরাং (+,-,*,/,= ,!=, <= , >=,<, >, && ,।।) এগুলো সবই এক একটা অপারেটর। তো জাভাস্ক্রিপ্ট  প্রোগ্রামিং এর ভাষায়  অপারেটর ১০ প্রকার তো আমি চেষ্টা করব এই দশপ্রকার অপারেটর গুলো যেন কিছু উদাহরণ দিয়ে তুলে ধরতে পারি তো কোমর বেঁধে প্রস্তুত হয়ে যান । 

- Assignment operators
- Comparison operators
- Arithmetic operators
- Bitwise operators
- Logical operators
- String operators
- Conditional (ternary) operator
- Comma operator
- Unary operators
- Relational operators



| Assignment                      | `x = y`    | `x = y`       |
| :------------------------------ | :--------- | :------------ |
| Addition assignment             | `x += y`   | `x = x + y`   |
| Subtraction assignment          | `x -= y`   | `x = x - y`   |
| Multiplication assignment       | `x *= y`   | `x = x * y`   |
| Division assignment             | `x /= y`   | `x = x / y`   |
| Remainder assignment            | `x %= y`   | `x = x % y`   |
| Exponentiation assignment       | `x **= y`  | `x = x ** y`  |
| Left shift assignment           | `x <<= y`  | `x = x << y`  |
| Right shift assignment          | `x >>= y`  | `x = x >> y`  |
| Unsigned right shift assignment | `x >>>= y` | `x = x >>> y` |
| Bitwise AND assignment          | `x &= y`   | `x = x & y`   |
| Bitwise XOR assignment          | `x ^= y`   | `x = x ^ y`   |
| Bitwise OR assignment           | `x |= y`   | `x = x | y`   |

**Assignment:** Assignment অপারেটর হলো যাকে আমরা বাংলায় সমান চিহ্ন ( = ) বলে জানি ছোট বেলা থেকে এটা অনেক ভাবে ব্যবহার করা যায় নিচে তা উল্লেখ করা হলো । 

Ex:   

```javaScript
১। const x = "Hello Bangladesh";
২। let y = 164.7;
৩। var z = true
```

উপরের সবগুলো **Assignment** এর উদাহরন

১। এর মানে হলো হলো x নামের মেমোরির কোন এক জায়গাতে   "Hello Bangladesh" কে রাখা হয়েছে। 

২। এর মানে হলো y নামের কোন এক জায়গাতে 164.7 কে রাখা হয়েছে ।

৩ এর মানে হলো z নামের কোন এক জায়গাতে true কে রাখা হয়েছে।

**Addition assignment:** Addition assignment বামদিকের অপারেন্ড এর সাথে ডানদিকের অপারেন্ডের যোগ করে  বামদিকের ভেরিয়্যাবল মধ্যে রাখাকে বুঝায়। মানে করি 

x = 10;

x = x+5 

x= 15;

এই কাজটা আরো সহজে করতে চাইলে 

x +=5 

x= 15

Ex:

```
let x = 10;
x +=10 //output: 20
let y = 4;
y += 5 //output: 5
```

**Subtraction assignment:** Subtraction assignment  Addition assignment এর বিপরীত কাজ করে অর্থাৎ বিয়োগ করার জন্য ব্যবহৃত হয় । বামদিকের অপারেন্ড এর সাথে ডানদিকের অপারেন্ডের বিয়োগ করে  বামদিকের ভেরিয়্যাবল মধ্যে রাখাকে বুঝায়। মানে করি 

x = 10;

x = x-5;

x= 5;

এই কাজটা আরো সহজে করতে চাইলে 

x -=5 

x= 5

```
let x = 10;
x -=10 //output: 20
let y = 4;
y -= 5 //output: 5
```



**অনুশীলন করুনঃ**

**Multiplication assignment,Division assignment ,Remainder assignment** এই তিন ধরনের অপারেটর দিয়ে তিনটা বা তার চেয়ে বেশি এক্সাম্পল করেন আর যদি করতে না পারেন কারো সাথে আলোচনা করেন অথবা গুগুল করেন অথাবা আমাকে জিজ্ঞাসা করেন।

**Exponentiation assignment:**  এই অপারেটর দেখতে নতুন হলেও কিন্তু এর কাজ যারা মাধ্যমিক স্কুলে পড়ালেখা করেছেন তাদের কাছে খুব পরিচিত । আমারা গনিতের কিছু সংখ্যক সমস্যা সমাধান করতে গিয়ে সুচক এর ব্যাপারে জেনেছিলাম এইটা টিক তার ই ব্যবহার।

অর্থাৎ আপনি যদি ২ এর বর্গ করতে চান তাইলে আপনাকে লিখতে হবে 

x= 5;

x= x**x;

আর এটাকে আপনি যদি আরো সহজে লিখতে চান তাইলে 

x **=x

Ex:

```
let x= 2;
let **=2; // 4 (Mean x= x**x)
```



