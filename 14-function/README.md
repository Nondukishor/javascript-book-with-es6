---
description: >-
  সতর্ক বার্তাঃ কেউ যদি বইটির কোন অংশ খারাপ উদ্দেশ্যে বা বাণিজ্যিক উদ্দেশ্য
  ব্যবহার  করে তাহলে কপিরাইট আইন অন্তর্ভুক্ত সকল প্রকার প্রক্রিয়া অনুসরণ করতে
  বাধ্য থাকব।
---

# ফাংশন (Function)

## ফাংশন

ফাংশন মানে হলো কাজ। আমাদের দৈনিক কাজটা কত বড় বা কেমন হবে সেটা নির্ণয় করা কঠিন হলেও প্রোগ্রামিং এর ক্ষেত্রে এইটা একটু ভিন্ন।  এখানে আপনি নির্ধারন করে দিতে পারবেন কোন ফাংশন কতটুকু কাজ করবে। বড় কাজ গুলো ছোট ছোট ফাংশন ভাগ করে নিতে পারবেন।  এবং সে কাজ গুলোকে বার বার ব্যবহার উপযোগী ও করে তুলতে পারবেন। একসময় জাভাস্ক্রিপ্ট শুধু মাত্র ফাংশন ভিত্তিক প্রোগ্রামিং ল্যাংগুয়েজ ছিল। ECMAScript আশার পর এতে ক্লাস যোগ করা হয়।&#x20;

এই অধ্যায়ে আমরা যেটা মূলত জানার চেষ্টা করব সেটা হলো

১। ফাংশন কি? এবং কিভাবে ফাংশন লিখা যায়?

২। ফাংশন কত প্রাকার ও কি ? কি ?

৩। অ্যারো ফাংশন কি? কিভাবে লেখা যায় ? এবং এর সুবিধা কি?

৪। কন্সট্রাক্টর ফাংশন কি?

৫। রিটান টাইপ ফাংশন?

৬। ফাংশন এর মাঝে আরগুমেন্ট বা প্যারামিটার পাস করা।

৭। উচ্চ আদেশ ফাংশন কি?

৮। কারিং ফাংশন কি?&#x20;

৯। রিকার্সিভ ফাংশন কি ও কিভাবে কাজ করে?&#x20;

১০। জেনেরেটর ফাংশন কি ও কিভাবে কাজ করে?&#x20;

## ফাংশন কি? এবং কিভাবে ফাংশন লিখা যায়?

ফাংশন মানে যে কাজ সেটা আগেই বলেছি।অর্থাৎ বড় বড় প্রোগ্রামের কোন নির্দিষ্ট কাজ কে ছোট ছোট কাজে ভাগ করে নেওয়াকে ফাংশন বলে। আপনি এইটাকে অনেকটা জুস মেশিনের সাথে তুলনা করতে পারেন। যেখানে আপনি কিছু একটা দিবেন আর ফলাফল স্বরূপ কিছু একটা পাবেন। সেটা হতে পারে undefined, null, string, number অথাবা অন্য কোন ভ্যালু এবার আসেন একটু দেখে নেই কিভাবে ফাংশন লিখতে হবে।

syntax:-

```javascript
//regular function syntex:
function nameOfFunction(argument){
//statement
    return something;
}
//arrow function syntex:
const nameofFunction=(argument)=>{
  //statement
    return something;
}
```

প্যারামিটার ও রিটার্ন টাইপের উপর ভিত্তি করে ফাংশন চার ভাগে ভাগ করা যায়। যথাঃ-

**১। Function without Argument and no return.**

**2। Function with Argument and no return.**

**৩। Function with Argument and return.**

**৪। Function without argument but return.**

**Function without Argument and no return:-** এইধরনের ফাংশনের ক্ষেত্রে কোন আরগুমেন্ট থাকে না এবং কোন রিটার্ন ভ্যালু ও থাকে না।

example:

```javascript
//function define

function isAdult(){
let age=18;
if(age>17){
  console.log("Yeah!, you are adult.")
 }
}

isAdult()//function call
```

এই ফাংশন এর মধ্যে আপনি লক্ষ্য করলে দেখতে পাবেন যে এইখানে কোন আরগুমেন্ট নাই এবং ফাংশনটা কোন কিছু রিটার্ন ও করতে পারছে না।

**Function with Argument and no return:-** এই ধরনের ফাংশনের ক্ষেত্রে আরগুমেন্ট থাকেলেও কো রিটান ভ্যালু থাকে না।

example:

```javascript
//function define
function isAdult(age){
   if(age>17){
     console.log("yeah! you are adult")
   }
}

isAdult(18); //function call and argumant passing
```

এই ফাংশনটা লক্ষ্য করলে দেখা যায় এতে একটি আর্গুমেন্ট আছে কিন্ত কোন রিটার্ন ভ্যালু নাই।

**Function with Argument and return:** function with argument and return টাইপের ফাংশনের ক্ষেত্রে ফাংশনের আরগুমেন্ট ও থাকে রিটার্ন ও থাকে । নিচে উদাহরনটি লক্ষ্য করুন।

```javascript
//function define 
function result(subject,gpa){
  return subject+":"+ gpa
}

result('Bangla',"5:00"); // function call


```
