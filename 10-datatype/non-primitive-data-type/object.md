---
description: 'Note: অবজেক্ট কিন্তু একটি নন প্রিমিটিভ ডাটা টাইপ মানে যা পরিবর্তন যোগ্য।'
---

# অব্জেক্ট (Object)

অব্জেক্ট মানে হচ্ছে বস্তু। কিন্তু প্রোগ্রামিং এর ভাষায় এইটা একটু ভিন্ন কনসেপ্ট বুঝায় তবে বিষয়টা অনেকটাই মিল মিল ব্যাপার আছে । এইখানে অব্জেক্ট বলতে অনেকগুলো কাল্পনিক ফাংশন এবং ভ্যারিএবলের সংমিশ্রন বলতে পারেন তবে সেইটা আবার বাস্তব জগতের কোন একটা সত্যিকার বস্তুর হবে ।&#x20;

ধরা যাক একটা চেয়ার একটা বস্তু । এখন আপনি যদি ঐ টা বৈশিষ্ট্য গুলো দেখেন তাহলে&#x20;

[১। চেয়ারটি কাঠ/ লোহা](#user-content-fn-1)[^1]/ প্লাস্টিক [দিয়ে তৈরি ](#user-content-fn-2)[^2]

২। চেয়ারটির ৪টি পা আছে

৩। চেয়ারের একটা রঙ আছে

৪। চেয়ারে বসা যায় কিনা ?



অবজেক্ট ও টিক এমন একটি বস্তুর বৈশিষ্ট্যের উপর ভিত্তি করে লিখা হয়। প্রতিটা অবজেক্ট অরিয়েন্টেড প্রোগ্রামিং ল্যাঙ্গুয়েজে অবজেক্ট বলতে এইটাই বুঝায়। চলুন দেখে  কোড করে দেখে নেই অবজেক্ট দেখতে এবং কেমন সেইটা কিভাবে লিখে।&#x20;

```
NOTE: অবজেক্ট লিখার নিয়ম
১। { (কার্লি ব্রাকেট) দিয়ে শুরু করতে হয় এবং }(কার্লি ব্রাকেট) দিয়ে শেষ করতে হয়।
২। কী এবং ভ্যালু আকারে লিখতে হয়।
৩। প্রতিটি কী ভ্যালু পেয়ারে এর পরে কমা ব্যাবহার করতে হয়। 
```



```javascript
const chair = {
               building_element: "iron",
               legs: 4,
               color: "brown",
               canSit: true
              }
```

এইখানে চেয়ার একটি অবজেক্ট এবং { } বন্ধনী এর ভিতরে যা লিখা আছে সব হলো তার বৈশিষ্ট্য । এই বৈশিষ্ট্য গুলোকে আমরা প্রোগ্রামিং এর ভাষায় বলি প্রোপার্টি। &#x20;

অবজেক্ট সাধারণত কী ভ্যালু আকারে থাকে । পরে যখন কোন ভ্যালু  এক্সেস করার দরকার হয় তখন এই কী দ্বারা এক্সেস করতে হয়।&#x20;

যেমনঃ-&#x20;

```javascript
console.log(chair.leg)
```

```
output
4
```

অবজেক্ট সবসময় প্রিমিটিভ ডাটা টাইপের  রেফারেন্স বহন করে থাকে।এঅবজেক্ট ব্যাবহার করে যে সুবিধাটা পাওয়া যায় সেটা হলো আপনি একই সাথে একের অধিক হাইব্রিড ডাটার সংমিশ্রন করতে পারেন।

উপরের chair অবজেক্টি লক্ষ্য করলে দেখবেন এইখানে বিভিন্ন ধরনের ডাটা টাইপ ব্যাবহার করা হয়েছে।

অবজেক্ট কিন্তু নেস্টেট (একটা অবজেক্ট এর ভিতরে আরেকটা অবজেক্ট) ভাবেও ব্যাভার করা যায় যেমন&#x20;

```javascript
const language = {
          bn:{
            indian_bangla: "Indian Bangla",
            bangoli: "Bangoli"
          },
         en:{
           usa: "USA"
           uk: "UK"
         }
 }
```

এইখানে উদাহরণটা দেখলে বুঝা যায় যে এইটি কিন্তু নেস্টেট অবজেক্ট হিসেবে লিখা হয়েছে  language একটা অবজেক্ট এবং এর ভিতরে bn , en আলাদা আলাদা দুইটা অবজেক্ট এইরকম চাইলে আমরা n লেবেল পর্যন্ত অবজেক্ট ব্যাবহার করতে পারি।&#x20;

অবজেক্ট এর কিছু বিল্ড ইন ফাংশন আছে সেগুলো আপনি কিভাবে ব্যাবহার করবেন সেইটা দেখে নেই ।



```javascript
// Creating an object
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
  hobbies: ["reading", "gaming", "swimming"],
};

// Object.keys() - Retrieve object keys as an array
const keys = Object.keys(person);
console.log("Keys:", keys); // Output: ["firstName", "lastName", "age", "hobbies"]

// Object.values() - Retrieve object values as an array
const values = Object.values(person);
console.log("Values:", values); // Output: ["John", "Doe", 30, ["reading", "gaming", "swimming"]]

// Object.entries() - Retrieve key-value pairs as arrays within an array
const entries = Object.entries(person);
console.log("Entries:", entries);
// Output:
// [["firstName", "John"], ["lastName", "Doe"], ["age", 30], ["hobbies", ["reading", "gaming", "swimming"]]]

// Object.assign() - Merge properties from multiple objects
const additionalInfo = {
  nationality: "American",
  occupation: "Software Engineer",
};

const mergedPerson = Object.assign({}, person, additionalInfo);
console.log("Merged Person:", mergedPerson);
// Output:
// {
//   firstName: "John",
//   lastName: "Doe",
//   age: 30,
//   hobbies: ["reading", "gaming", "swimming"],
//   nationality: "American",
//   occupation: "Software Engineer"
// }

// Object.hasOwnProperty() - Check if an object has a specific property
const hasAge = person.hasOwnProperty("age");
console.log("Has age property?", hasAge); // Output: true
const hasGender = person.hasOwnProperty("gender");
console.log("Has gender property?", hasGender); //

```





[^1]: 

[^2]: 
