# অসমনিয়ত ও অপেক্ষা (Async & Await)

Async শব্দের অর্থ হলো অসমনিয়ত মানে হলো আপনি এমন কোন কাজ করতে চাইছেন যেইটা আসলে এক্টার পর একটা হবে না না বা সিরিয়ালি হবে না। তাহলে কেমন করে হবে?&#x20;

তাহলে বিষয়টা গল্প করে বলি ধরুন আপনি কোন একটা কুরিয়ার সার্ভিস কোম্পানি ধরে নিলাম আপনার কোম্পানির নাম হচ্ছে **আত্মবিশ্বাস** এখন আপনি অনেকের কাজ থেকে পন্য নেন এবং তাদের গন্তব্য স্থলে পৌছে দেন। এই যে কাজ **আত্মবিশ্বাস** কোম্পানি করে সেইটা কিন্তু সিরিয়ালি হচ্ছে না কেন? ধরুন **দিলদার** নামে একজন ১১ তারিখ সকাল ১০ঃ০০ টায় পন্য কুরিয়ার সার্ভিসে জমা দিয়েছে যার গন্তব্য স্থল হচ্ছে **চট্টগ্রামের কাপ্তাই** এলাকা আর **বাপ্পারাজ** তার বউয়ের জন্য শাড়ি পাঠিয়েছে যেইটা **রাঙ্গামাটি এলাকা** জমা দেওয়ার সময় ছিল ১১ তারিখ সকাল ৯ঃ০০ টা আর **জসিম সাহেব** বউয়ের জন্য সেলাই মেশিন পাঠিয়েছে যেইটা চট্টগ্রামের **বদ্দার হাট** এলাকা জমা দেওয়ার সময় ছিল একই তারিখে সকাল ১২ঃ০০টা এখন আপনার **আত্মবিশ্বাস** কোম্পানির লোকেশন  হচ্ছে ঢাকা গুলশান-১ । আপনি যখন পন্য নিয়ে রওনা দিলেন আপনি এখন কার টা ডেলিভারি দিবেন? অবস্যই যার লোকেশন আপনার যাওয়ার সময় সামনে পাবেন বা কাছে হবে। ধরে নিলাম আপনার অফিস থেকে যাদের জিনিস ডেলিভারি দিবেন তাদের বাসার দূরত্ব হচ্ছেঃ-

<table data-full-width="false"><thead><tr><th>আপানার কোম্পানি লোকেশন</th><th>গন্তব্য দূরত্ব</th><th>গন্তব্য এর নাম</th></tr></thead><tbody><tr><td><strong>আত্মবিশ্বাস গুলশান-১</strong></td><td>৩০১ কিঃ মিঃ </td><td><strong>কাপ্তাই(দিলদার)</strong></td></tr><tr><td><strong>আত্মবিশ্বাস গুলশান-১</strong></td><td>৩০৬ কিঃ মিঃ </td><td><strong>রাঙ্গামাটি(বাপ্পারাজ)</strong></td></tr><tr><td><strong>আত্মবিশ্বাস গুলশান-১</strong></td><td>২৫২ কিঃ মিঃ</td><td><strong>বদ্দার হাট(জসিম)</strong></td></tr></tbody></table>

এখন আপনি আপনি আশা করি বুঝে নিয়েছেন যে কার টা আগে ডেলিভারি হবে তো উত্তর হচ্ছে জসিম কেন? কারণ জসিমের বসার দূরত্ব কম তাই জসিম আগে পাবেন। তারপর দিলদার সাহেবের তারপর বাপ্পারাজ । আর এই যে পুরো বিষয় টা এইটায় হচ্ছে Async বা Asynchronous ।

এবার আসি আসল কথায় আমারা এর আগেই জেনেছি প্রমিস নামে এমন একটা জিনিস আগে থেকেই আছে থাহলে আমারা Async লিখতে যাচ্ছি কেন?

উত্তর হচ্ছে আমরা আসলে প্রমিসের যে সিন্ট্যাক্স সেটাকে ছোট করে লেখার জন্য এমন টা করেছি বা আমাদের কোন ফাংশনে যাতে আমরা খুব সহজে প্রমিস বিষয় টা যুক্ত করতে পারি তার জন্য এমন টা করেছি।&#x20;

তাহলে এবার একটা উদাহরণ দেখে নেই কিভাবে লিখে Async ফাংশন&#x20;

{% code title="Async with Regular function" overflow="wrap" lineNumbers="true" %}
```javascript
async function regularFunction() {
 //statement
}

```
{% endcode %}



{% code title="Async with arrow function" lineNumbers="true" %}
```javascript
const arrowAsyncFunction = async () => {
  //statement
};

```
{% endcode %}



{% code title="Async with member function" overflow="wrap" lineNumbers="true" %}
```javascript
class MyClass {
  async classAsyncMethod() {
    //statement
  }
}

```
{% endcode %}

এখন ফাংশন তো লিখে ফেললেন সেইটা কল করবেন কিভাবে তাও একটা ব্যাপার আছে। Async কল করার দুইটা উপায় আছে একটা হচ্ছে প্রমিসের মতো করে মেথড চেইনিং আরেকটা হচ্ছে await চলুন দেখে নেই সেগুলো।

{% code overflow="wrap" lineNumbers="true" fullWidth="false" %}
```javascript
//with regular function
async function sum() {
  return 2+3
}

//With Promise syntex
sum.then(function(response){
  return response;
})

//with await syntex
const result = await sum()

// with arrow function
const sum = async ()=>{
 return 2+2;
}

//Promise syntex
sum.then(res=>console.log(res))

// await syntext 
const result = await sum()
console.log(result)


// with class member functions
class Mathmatic{
   async sum(){
     return 3+3;
   }
}

const math = Mathmatic()

//Promise Syntex
math.sum().then(res=>console.log(res))

//await syntex
const result = await math.sum()
console.log(result)
```
{% endcode %}

