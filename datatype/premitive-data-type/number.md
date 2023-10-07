# নাম্বার (Number)

**নাম্বারঃ-** মজার একটা ডাটাটাইপের নাম হলো নাম্বার। অন্যান্য ল্যাংগুয়েজ হয়তো এই নাম্বার কে ভাগ করা হয়েছে ইন্টিজার (পূর্ণ সংখ্যা) ফ্লোট নাম্বার(দশমিক যুক্ত সংখ্যা) ডাবল নাম্বার ইত্যাদি কিন্তু জাভাস্ক্রিপ্টে এই সব কিছু কে একটা ডাটাটাইপ হিসেবে দেখানোা হয়েছে। আর সেটা হলো নাম্বার। কম্পিউটার ভাইয়া কে আপনি যতই বলেন এই নাম্বার ঐ নাম্বার জাভাস্ক্রিপ্ট কম্পিউটার ভাইয়াকে বুঝায় দিবে সবগুলো কিন্তু নাম্বার ডাটা টাইপ।&#x20;

সুতরাং মোটকথা হলো জাভাস্ক্রিপ্ট এ আপনি বাইনারী, দশমিক ,হেক্সাডেসিমেল এবং ইন্টিজার সবকিছুর জন্য একটা ডাটা টাইপ পাচ্ছেন আর সেইটা হলো নাম্বার।&#x20;

একটা উদাহরণ না দেখলে মনে আবার কষ্ট পাবেন তাই একটা হাতে কড়ি করে নেই।

{% code title="number.js" overflow="wrap" lineNumbers="true" %}
```javascript
var number1=10; //integer
var number2=11.05; // decimal/float
var number3=0xff;//hexadecimal
var number4=0b11111111;//binary
var number5=0.255e3 //decimal exponential notation

console.log(typeof number1,typeof number2, typeof number3, typeof number4, typeof number5)
```
{% endcode %}

output:

```javascript
number number number number number
```

#### NaN - Not a Number:

NaN এর পুরো অর্থ হলো Not a Number। যখন জাভাস্ক্রিপ্ট নাম্বারকে Identify করতে পারে না তখন সে সেটাকে NaN হিসবে চিহ্নিত করে নেয়। NaN কে চেক করার জন্য জাভাস্কিপ্টে একটা প্রি-বিল্ট মেথড আছে isNaN নামে।

চলুন একটা উদাহরণ দেখে নেইঃ

{% code lineNumbers="true" %}
```javascript
console.log(isNaN(123));       // false
console.log(isNaN("one"));     // false
```
{% endcode %}

#### চলুন জেনে নিই কখন কখন NaN হয় ?

* **গাণিতিক অপারেশনের ক্ষেত্রেঃ-**

```javascript
console.log(0 / 0);    // NaN
console.log(Math.sqrt(-1));    // NaN
```

* **ডাটা পার্সিং এর ক্ষেত্রেঃ-**

```javascript
console.log(parseInt("Hello"));   // NaN
```

* **ডাটা ক্যালকুলেশনের ক্ষেত্রেঃ-**&#x20;

```javascript
console.log(NaN + 5);   // NaN
```

#### Infinity

Infinity জাভাস্ক্রিপ্টে একটি বিশেষ নিউমেরিক ভ্যালু। Infinity সাধারণত যেকোনো নাম্বার থেকে বড় নাম্বারকে বুঝায়। Infinity ধনাত্মক বা ঋণাত্মক উভয় হতে পারে। Infinity শব্দের অর্থ হলো অসীম যার মানে হলো সীমাহীন।&#x20;

_চলুন কিছু উদাহরণ এর মাধ্যমে দেখে নেইঃ-_&#x20;

{% code lineNumbers="true" %}
```javascript
console.log(1 / 0);     // Infinity
console.log(-1 / 0);    // -Infinity
```
{% endcode %}

জাভাস্ক্রিপ্টে সর্বোচ্ছ নাম্বার রিপ্রেজেন্টশন পাস করলে মানে পার্সিং ওভার ফ্লো হলে Infinity হয়।&#x20;

{% code lineNumbers="true" %}
```javascript
console.log(parseFloat("1e309"));   // Infinity
```
{% endcode %}

#### Hexadecimal:

জাভাস্ক্রিপ্টে 0x প্রিফিক্স যুক্ত করার মাধ্যমে হেক্সাডেসিমেল লিখা হয় । ০ -৯ এর পরের সংখ্যা গুলোকে A-F  দিয়ে প্রকাশ করা হয়।&#x20;

উদাহরণঃ-

{% code lineNumbers="true" %}
```javascript
let hexNumber = 0x1A; // This represents the decimal number 26
console.log(hexNumber); // Outputs: 26
```
{% endcode %}

#### Number Object JavaScript:&#x20;

#### JavaScript Number Methods:
