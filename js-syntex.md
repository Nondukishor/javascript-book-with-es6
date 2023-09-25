---
description: >-
  সতর্ক বার্তাঃ কেউ যদি বইটির কোন অংশ খারাপ উদ্দেশ্যে বা বাণিজ্যিক উদ্দেশ্য
  ব্যবহার  করে তাহলে কপিরাইট আইন অন্তর্ভুক্ত সকল প্রকার প্রক্রিয়া অনুসরণ করতে
  বাধ্য থাকব।
---

# সিনট্যাক্স নিয়ে যত কথা।

জাভাস্ক্রিপ্ট একটি কম কড়াকড়ি মানে (loosely) টাইপ ল্যাঙ্গুয়েজ।এইটি অন্যান্য ল্যাঙ্গুয়েজের মতো খুব বেশি case sensitive না। এটার কারণে অবশ্য অনেক সময় বিপাকে  পড়তে হয় । তবে **"use strict"** নামে **literal expression** ব্যবহার করলেও অনেকটা স্ট্রিক্ট মুডে প্রোগ্রাম রান করানো যায় । জাভাস্ক্রিপ্ট তিন রকম ভাবে লিখা যায়।

1. **Inner Script**
2. **Inline Script**
3. **External Script File**



#### **Inner Script**

```html
First Syntex:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> প্রথম প্রোগ্রাম হ্যাঁলো বাংলাদেশ </title>
</head>
<body>
   
    <script>
        console.log('হ্যাঁলো বাংলাদেশ');
    </script>
</body>
</html>
```

প্রথমে এখানে যা করা হয়েছে সেটি হলো । .html extension সংযোগে যেকোনো নামের একটা ফাইল বানানো হয়েছে সেটা হতে পারে index.html সেটা হতে পারে firstProgramSyntex.html বা আপানার পছন্দ অনুযায়ী নামের । HTML-5 এর কিছু কোড লিখা হয়েছে । তারপর নিচের দিকে একটু লক্ষ্য করলে দেখতে পারবেন নামের একটা ট্যাগ লিখা হয়েছে এবং তার মধ্যে কোড লিখা হয়েছে console.log('হ্যাঁলো বাংলাদেশ'); এবার আপনি রান করেন তাইলে ব্রাউজারে কিছু দেখতে পাবেন না পাবেন কেমন করে আউট পুট তো কনসোলে আছে তাহলে আপনি যদি ক্রোম ব্যবহারকারী হয়ে থাকেন তাহলে f12 press করেন । আর তাহলে ওপেন হয়ে যাবে কনসোল আর দেখতে পাবেন আউটপুট ।

```reStructuredText
হ্যাঁলো বাংলাদেশ
```

#### Inline Script

```html
Second syntex:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> দ্বিতীয় প্রোগ্রাম আমি তোমায় ভালবাসি </title>
</head>
<body>
    <form>
        <button onclick="return confirm('আমি তোমায় ভালবাসি')">
           ক্লিক করে জেনে নিন  
        </button>
        <!--javascript in inner tag -->
    </form>
</body>
</html>

```

আগের মতো একটা পছন্দ অনুযায়ী নামে ফাইল বানিয়ে নেওয়া হয়েছে । HTML-5 এর কিছু কোড লিখা হয়েছে । তারপর ট্যাগের ভিতরে লক্ষ্য করলে দেখতে পাবেন নামে আরেকটা ট্যাগ আছে । এই বাটন তো আপনার সার্টের বাটন না এটা HTML এর ট্যাগ বাটন এটাতে দিকে একটু লক্ষ্য করলে দেখতে পারবেন onclick attribute এর সাথে কিছু কোড লিখা হইয়েছে নামের একটা ট্যাগ লিখা হয়েছে এবং তার মধ্যে কোড লিখা হয়েছে console.log('আমি তুমায় ভালবাসি'); এবার আপনি আগের মত করে রান করেন তাইলে আউটপুট দেখতে পারবেন।আমি তুমায় ভালবাসি&#x20;

```html
<!--Third Syntext:-->
<!--index.html:-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> তৃতীয় প্রোগ্রাম বাংলাদেশ সবুজ শ্যামল দেশ  </title>
</head>
<body>
  <script src="index.js"></script>
</body>
</html>
```

```javascript
//index.js
<!-- js file include from spearate file with .js extenstion-->
console.log('বাংলাদেশ সবুজ শ্যামল দেশ');
```

এই প্রোগ্রামের জন্য যা করা হয়েছে প্রথমে আগের মতো একটি HTML ফাইল বানানো হয়েছে তাতে কিছু HTML-5 এর কোড লিখা হয়েছে। নিচের দিকে তাকালে দেখবেন index.js একটা ফাইল তৈরি করা হয়েছে । আর সেইটা তে console.log('বাংলাদেশ সবুজ শ্যামল দেশ'); লিখাটা লিখা হয়েছে। এবার এই index.js ফাইল টিকে যুক্ত করে নিতে হবে । কেমন করে করবেন এত বড় কঠিন কাজ ? আরে বাবা ! এত কঠিন না শুধু লিখতে হবে ১৩ নাম্বার লাইনের মতো করে তারপর ইমপ্লিমেন্ট করে দিতে হবে সেই ফাইলটি আর ব্যস রান করিয়ে নিন ।এখন আপনার কাজ হচ্ছে আপনি এইরকম আরো কিছু প্রোগ্রাম লিখবেন যেখানে আপনি আপনার প্রিয় দুইজন মানুষ এবং আমাদের দেশকে নিয়ে লিখবেন। তো শুরু করে দিন আর লিখা শেষ হলে আমাকে মেইল করে জানিয়ে দিন pro.nipu@gmail.com এই মেইলে মাধ্যমে।
