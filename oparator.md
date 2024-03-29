---
description: >-
  সতর্ক বার্তাঃ কেউ যদি বইটির কোন অংশ খারাপ উদ্দেশ্যে বা বাণিজ্যিক উদ্দেশ্য
  ব্যবহার  করে তাহলে কপিরাইট আইন অন্তর্ভুক্ত সকল প্রকার প্রক্রিয়া অনুসরণ করতে
  বাধ্য থাকব।
---

# অপারেটর

অপারেটর মানে হলো যে অপারেশন করে মানে যে কাজ অপারেট করে থাকে । আমরা গনিতে যে অপারেটর গুলো নিয়ে পড়ালেখা করে এসেছি সেগুলোই আবার এইখানে ব্যবহার করব তাই এইখানে তেমন কঠিন কিছু নাই । অনেকেই অনেক ভাবে বলে আমি যেভাবে অপারেটর কে সংজ্ঞায়িত করে থাকি তা হলো অপারেটর হলো ঘটক এর মতো যে বর কনে এর মাঝে সম্পর্ক স্থাপন করে দেয় । সুতরাং (+,-,\*,/,= ,!=, <= , >=,<, >, && ,।।) এগুলো সবই এক একটা অপারেটর। তো জাভাস্ক্রিপ্ট প্রোগ্রামিং এর ভাষায় অপারেটর ১০ প্রকার তো আমি চেষ্টা করব এই দশপ্রকার অপারেটর গুলো যেন কিছু উদাহরণ দিয়ে তুলে ধরতে পারি তো কোমর বেঁধে প্রস্তুত হয়ে যান ।

* Assignment operators
* Comparison operators
* Arithmetic operators
* Bitwise operators
* Logical operators
* String operators
* Conditional (ternary) operator
* Comma operator
* Unary operators
* Relational operators

| নাম                                                                                                                   | সংক্ষিপ্ত রুপ | বর্ধিত রূপ    |
| --------------------------------------------------------------------------------------------------------------------- | ------------- | ------------- |
| Assignment(নিয়োগ)                                                                                                     | `x = y`       | `x = y`       |
| Addition assignment(সংযোজন নিয়োগ)                                                                                     | `x += y`      | `x = x + y`   |
| Subtraction assignment (বিয়োগ নিয়োগ)                                                                                  | `x -= y`      | `x = x - y`   |
| Multiplication assignment(গুণ বরাদ্দকরণ)                                                                              | `x *= y`      | `x = x * y`   |
| Division assignment(ভাগ বরাদ্দকরণ )                                                                                   | `x /= y`      | `x = x / y`   |
| Remainder assignment(অবশিষ্ট নিয়োগ)                                                                                   | `x %= y`      | `x = x % y`   |
| Exponentiation assignment(সূচক নিয়োগ)                                                                                 | `x **= y`     | `x = x ** y`  |
| Left shift assignment(বাম পরিবর্তন নিয়োগ)                                                                             | `x <<= y`     | `x = x << y`  |
| Right shift assignment(ডান পরিবর্তন নিয়োগ)                                                                            | `x >>= y`     | `x = x >> y`  |
| Unsigned right shift assignment(অস্বাক্ষরিত ডান নিয়োগ ) _<mark style="color:red;">**`0 থেকে ধনাত্মক সংখ্যা`**</mark>_ | `x >>>= y`    | `x = x >>> y` |
| Bitwise AND assignment (বিট অনুযায়ী এবং নিয়োগ)                                                                        | `x &= y`      | `x = x & y`   |
| Bitwise XOR assignment(বিট অনুযায়ী একচেটিয়াভাবে অথবা নিয়োগ)                                                           | `x ^= y`      | `x = x ^ y`   |
| Bitwise OR assignment(বিট অনুযায়ী অথবা নিয়োগ)                                                                         | x \|= y       | x = x \| y    |

**Assignment:** Assignment অপারেটর হলো যাকে আমরা বাংলায় সমান চিহ্ন ( = ) বলে জানি ছোট বেলা থেকে এটা অনেক ভাবে ব্যবহার করা যায় নিচে তা উল্লেখ করা হলো ।

Ex:

```javascript
১। const x = "Hello Bangladesh";
২। let y = 164.7;
৩। var z = true
```

উপরের সবগুলো **Assignment** এর উদাহরন

১। এর মানে হলো হলো x নামের মেমোরির কোন এক জায়গাতে "Hello Bangladesh" কে রাখা হয়েছে।

২। এর মানে হলো y নামের কোন এক জায়গাতে 164.7 কে রাখা হয়েছে ।

৩ এর মানে হলো z নামের কোন এক জায়গাতে true কে রাখা হয়েছে।

**Addition assignment:** Addition assignment বামদিকের অপারেন্ড এর সাথে ডানদিকের অপারেন্ডের যোগ করে বামদিকের ভেরিয়্যাবল মধ্যে রাখাকে বুঝায়। মানে করি

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

**Subtraction assignment:** Subtraction assignment Addition assignment এর বিপরীত কাজ করে অর্থাৎ বিয়োগ করার জন্য ব্যবহৃত হয় । বামদিকের অপারেন্ড এর সাথে ডানদিকের অপারেন্ডের বিয়োগ করে বামদিকের ভেরিয়্যাবল মধ্যে রাখাকে বুঝায়। মানে করি

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

**Exponentiation assignment:** এই অপারেটর দেখতে নতুন হলেও কিন্তু এর কাজ যারা মাধ্যমিক স্কুলে পড়ালেখা করেছেন তাদের কাছে খুব পরিচিত । আমারা গনিতের কিছু সংখ্যক সমস্যা সমাধান করতে গিয়ে সুচক এর ব্যাপারে জেনেছিলাম এইটা টিক তার ই ব্যবহার।

অর্থাৎ আপনি যদি ২ এর বর্গ করতে চান তাইলে আপনাকে লিখতে হবে

x= 5;

x= x\*\*x;

আর এটাকে আপনি যদি আরো সহজে লিখতে চান তাইলে

x \*\*=x

Ex:

```javascript
let x= 2;
x **=2; // 4 (Mean x= x**x)
```

{% hint style="info" %}
( \*\* ) অপারেটরটার নাম হচ্ছে সূচক (Exponentiation) অপারেটর&#x20;
{% endhint %}
