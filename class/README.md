---
description: >-
  সতর্ক বার্তাঃ কেউ যদি বইটির কোন অংশ খারাপ উদ্দেশ্যে বা বাণিজ্যিক উদ্দেশ্য
  ব্যবহার  করে তাহলে কপিরাইট আইন অন্তর্ভুক্ত সকল প্রকার প্রক্রিয়া অনুসরণ করতে
  বাধ্য থাকব।
---

# ক্লাস ও অবজেক্ট অরিয়েন্টেড (class & OOP)

ক্লাস মানেই যে আপনাকে বই খাতা নিয়ে স্কুল বা কলেজে যেতে হবে তা নয় কিন্তু । ক্লাস মানে এখানে একটা হাবিজাবি প্রোগ্রামিং এর ভাষায় লিখা। মানে কিছু লিখব আর সেটা কিছু করবে। অনেকটা আলাউদ্দিনের প্রদীপ এর ঝিনের মত যা নির্দেশ দিব সে করে ফেলবে জটপট দেরি না করে। পার্থক্য শুধু আলাউদ্দিনের প্রদীপ এর ঝীন ৩টা ইচ্ছা পূরণ করে আর আমাদের ক্লাস অসংখ্য ইচ্ছা পূরণ করবে। তাহলে মনে প্রশ্ন জাগতে পারে ক্লাস কাকে বলে? আমাকে যদি কেউ জিজ্ঞাসা করে আমি কি এটা বলে দিব ? উত্তর হলো দিতে পারেন তবে আরেকটু পড়ে জেনে বুঝে উত্তর দিলে খাপে খাপ কমালার বাপ হয় যাবে একদম । তাহলে আসেন সেটা কিভাবে জেনে নেই ।

অন্যান্য ক্ষেত্রের থেকে জাভাস্ক্রিপ্টে ক্লাসের বিষয়টা একটু ভিন্ন। জাভাস্ক্রিপ্টে ক্লাস টাও একটা ফাংশন । ECMAScript 2015 এর পর থেকে জাভাস্ক্রিপ্টে ক্লাস বৈশিষ্ট্য যুক্ত করা হয়। সুতরাং ক্লাস হচ্ছে জাভাস্ক্রিপ্টে স্পেশাল একটা ফাংশন। যেখানে আপনি ফাংশন লিখতে পারবেন প্রোপার্টি যুক্ত করতে পারবেন। অন্য আরেকটি ক্লাসের প্রোপার্টি ইনহেরিট করতে পারবেন। সুবিধা মত ব্যবহার করতে পারবেন । কিন্তু যদি প্রোগ্রামিং কে অনুসরন করে বলতে যায় ক্লাস হচ্ছে ইউজার ডিফাইন্ড ডাটাটাইপ যেখানে ইউজার তাদের তাদের প্রয়োজনীয় ডাটা গুলো লিখে রাখে এবং প্রয়োজনে ব্যবহার করে থাকে।\
\
MDN অফিশিয়াল সাইটে ক্লাস সম্পর্কে যা বলা হয়েছে&#x20;

_<mark style="color:orange;">**Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on**</mark>_ [_<mark style="color:orange;">**prototypes**</mark>_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance\_and\_the\_prototype\_chain) _<mark style="color:orange;">**but also have some syntax and semantics that are unique to classes.**</mark>_

\
অর্থাৎ ক্লাস অবজেক্ট তৈরি করার জন্য একটি টেমপ্লেট। তারা সেই ডেটাতে কাজ করার জন্য কোড সহ ডেটা এনক্যাপসুলেট করে। JS-এর ক্লাসগুলি প্রোটোটাইপের উপর নির্মিত কিন্তু কিছু সিনট্যাক্স এবং নিজস্ব কিছু বৈশিষ্ট্য  রয়েছে যা ক্লাসের জন্য অনন্য।

ক্লাস কিভাবে লিখে সেটা একটু দেখে নেই ...

```javascript
class Book{
   constructor(){
   this.property_1;
   this.property_2;
   this.property_3;
   }
  
  func_1(){
  
  }
  func_2(){
  
  }
  
  func_3(){
  
  }
  
  -------------------
  ------------------
  func_n(){
  
  }
  
}
```

আচ্ছা কিভাবে লিখতে তা তো দেখলাম এখন আমারা দেখব কতভাবে ক্লাস Declare  করা যায়&#x20;

```javascript
// বেসিক Decleartion
class Animal {
  constructor(leg, size, color) {
    this.leg = leg;
    this.size = size;
    this.color = color;
  }
}

// Expression; Variable এ ক্লাস decleartion
const Animal = class {
  constructor(leg, size, color) {
    this.leg = leg;
    this.size = size;
    this.color = color;
  }
}

// Expression; ক্লাসের নাম দিয়ে ক্লাস decleartion
const Animal = class AnimalClass {
  constructor(leg, size, color) {
    this.leg = leg;
    this.size = size;
    this.color = color;
  }
}

```

ক্লাস শুরু হয় কিন্তু  ২য় বন্ধনি বা curly brackets <mark style="color:green;">`{ }`</mark>দিয়ে। এর মাঝেই আপনাকে লিখতে হবে আপনি ক্লাসে যে কাজ গুলো করতে চান । সেইটা হতে পারে মেম্বার ফাংশন অথবা কন্সট্রাক্টর ফাংশন।চলুন আরেকটা উদাহরণ দেখে নেইঃ&#x20;

```javascript
class Person{
  //constructor function
  constructor(name, age, height){
     this.name = name;
     this.age = age;
     this.height = height;
  }
  
  //member function which show name of person
  showName(){
    return this.name;
  }
  
  //member function which show age of person
  showAge(){
    return this.age;
  }
  
  //member function which show height of person
  showHeight(){
    return this.height;
  }
  
}
```
