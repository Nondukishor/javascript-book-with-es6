# স্ট্রিং (String)

**স্ট্রিংঃ-** স্ট্রিং প্রোগ্রামিং এর ক্ষেত্রে খুবই গুরুত্ব পূর্ণ একটা ডাটা টাইপ এবং প্রতি পদে পদে এটা ব্যাবহার করতে হবে আপনাকে। ডাবল কোটেশন বা সিঙ্গেল কোটেশনে যা লিখা হয় তাই স্ট্রিং তবে আরেক ভাবে লিখে যায় সেইটা হচ্চে [Backtick](https://en.wikipedia.org/wiki/Backtick) এর মাধ্যমে । তবে যদি বলতে যায় আরো ক্লিয়ার করে অনেকগুলো ক্যারেক্টার এর সমন্বিত রুপ হচ্ছে স্ট্রিং। একথায় ক্যারেক্টার বা বর্ণগুচ্ছ এর মানে হচ্ছে স্ট্রিং আর এটা লিখতে কোটেশন মার্ক বা চিহ্ন এর ভিতরে ।

{% code lineNumbers="true" %}
```javascript
var myName = 'Nipu Chakraborty';
let address= 'Chottogram,Rungunia';
const mobileNumber = "+8801xxxxxxxxxxxx";
const value = `My address is ${address} and Mobile Number is: ${mobileNumber}`;
```
{% endcode %}

উপরে যে লাইন কয়েক কোড দেখছেন সবই স্ট্রিং। চলুন আরো কিছু উদাহরণ দেখে নেই।&#x20;

#### স্ট্রিং এর দৈর্ঘ্য কত?

স্ট্রিং এর দৈর্ঘ্য যাচাই করার জন্য জাভাস্ক্রিপ্টে একটি বিল্ড ইন প্রোপার্টি আছে আছে সেটি হচ্ছে `length`&#x20;

এই প্রোপার্টিটা দিয়ে জাভাস্ক্রিপ্ট একটা স্ট্রিং এর দৈর্ঘ্য কতটুকু বা কত লম্বা সেইটা বের করা যায়।&#x20;

```javascript
const name = "Nipu"
console.log(name.length);// 4
```

**স্ট্রিং কি আসলেই একটা অ্যারে ?**

{% code lineNumbers="true" %}
```javascript
const word = "JavaScript";
const firstLetter = word[0]; // J
const lastLetter = word[word.length - 1]; // t
```
{% endcode %}

উপরের উদাহরন এর মধ্যে আমরা দেখতে পাচ্ছি আমরা যেভাবে অ্যারে এক্সেস করি ঠিক সেভাবে স্ট্রিং এক্সেস করেছি। এতে করে আমারা বলতেই পারি স্ট্রিং হচ্ছে অনেকগুলো বর্ণের সমষ্টি ।&#x20;

চলুন আরো কিছু উদাহরন দেখি

#### কিভাবে দুইটা স্ট্রিং কে যুক্ত করা যায়?

দুইটি স্ট্রিং কে সাধারণত যোগ চিহ্ন দিয়ে যুক্ত করা যায় কিন্তু আপনি চাইলে আরো একভাবে এই কাজটি করা যায় সেইটা হলো Template Strings। এইটা করার জন্য আপনাকে ব্যাবহার করতে হবে back-ticks (\`\`) symbol ব্যাবহার করতে হবে। আর ভিতরে কোন ভ্যারিয়েবল স্ট্রিং লিখার জন্য ${variableName} এইভাবে লিখতে হবে।&#x20;

{% code lineNumbers="true" %}
```javascript
const firstName = "John";
const lastName = "Doe";
const fullName = firstName + " " + lastName;
```
{% endcode %}

### কোন পজিশনে কোন স্ট্রিং আছে?

একটা স্ট্রিং এর কোন পজিশনে কোন charecter আছে সেইটা বের করার জন্য জাভাস্ক্রিপ্টে একটা বিল্ড ইন মেথড আছে charAt(string\_position) নামে যেইটা মূলত স্ট্রিং পজিশন নিয়ে সেই পজিশনের charteter টা রিটার্ন করে দেয়।&#x20;

{% code lineNumbers="true" %}
```javascript
const myName = "Nipu Chakraborty";
console.log(myName.charAt(0)) // N
console.log(myName.charAt(1)) // i
console.log(myName.charAt(2)) // p
console.log(myName.charAt(3)) // u
```
{% endcode %}

উপরের কোডটা দেখলে বুঝতেই পারবেন যে charAt মেথড টা প্রতিবার পজিশন অনুযায়ী স্ট্রিং ক্যারেক্টার রিটার্ন করছে।&#x20;

### অনুশীলনঃ-&#x20;

নিজের মেথড গুলো কি কাজ করে এবং কিভাবে ব্যাবহার করা যায় সে সম্পর্কে বিস্তারিত জানা।&#x20;

```javascript
String charCodeAt()
String at()
String [ ]
String slice()
String substring()
String substr()
String toUpperCase()
String toLowerCase()
String concat()
String trim()
String trimStart()
String trimEnd()
String padStart()
String padEnd()
String repeat()
String replace()
String replaceAll()
String split()
```

