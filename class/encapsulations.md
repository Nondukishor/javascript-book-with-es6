# এনসকেপসুলেশন (Encapsulations)



<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>এনসকেপসুলেশন</p></figcaption></figure>

ছবির রেফারেন্সঃ [https://algodaily.com/lessons/understanding-encapsulation-in-programming/introduction](https://algodaily.com/lessons/understanding-encapsulation-in-programming/introduction)

আশা করি চিত্রটি দেখার পরে অনেকের কাছেই বিষয়টা অনেক সহজ আর হয়ত অনেকেই ধারণা করতে পেরেছেন। যে আসলে বিষয়টা কি?&#x20;

এনকেপসুলেশন বিষয়টা একদমই আমাদের দৈনন্দিন জীবনের সাথে খুবই জড়িত। মনে করুন আপনি একটা ক্যাপসুল কিনবেন সেইখানে দেখবেন ক্যাপসুল টা দুইটা ক্যাপ দিয়ে ক্যাপসুল টা আবৃত এবং ভিতরে হরেক রকম দানাদার পাউডার আছে। এখন মনে করে নিন আপনার গ্যাসের সমস্যা হয়েছে আর আপনার একটা গ্যাসের ক্যাপসুল খাওয়ার লাগবে ঐ ক্যাপসুলের ভিতরে অনেক গুলো ফাংশনাল দানাদার পদার্থ আছে। আবার কিছু জিনিস আছে সেগুলোর সাহায্যকারী উপদান।  মনে করে নিলাম ফাংশনাল বিষয় বস্তু গুলো হচ্ছে মেম্বার ফাংশন আর সেগুলো সাহায্যকারী উপদান সেগুলো হচ্ছে ভ্যারিএবল। আর এই পুরো বিষয়বস্তুগুলো মিলে যে জিনিসটা তৈরি হয় সেইটায় হচ্ছে এনকেপসুলেশন আর সেইটা একটা ক্লাস কে কেন্দ্র করে হচ্ছে। এখন কথা হচ্ছে ভাই আমায় কি ভূতে কিলায়ছে ! যেখানে আমি ফাংশন লিখতে পারব। আলাদা করে ভ্যারিএবল লিখতে পারব।  কি দরকারে ক্লাস লিখব। আবার উদ্ভট একটা কি ক্যাপসুল হাবিজাবি শিখতে যাব আমার কি আর খাই দাই কাজ নাই ?উত্তর হচ্ছে আপনি চাইলে ফাংশন দিয়ে করতে পারেন কিন্তু অবজেক্ট অরিয়েন্টেড এ করতে হলে এভাবেই করা লাগবে।

কিন্তু তখন আপনি আবার বলবেন কেন? কেন? এবং কেন? চলুন তাহলে আরেকটু সুড়ঙ্গ খুড়ে বের করি কেন? কেন? এবং কেন?। ধরুন আপনি একটা ভেরিয়েবল লিখলেন person = " A real man :) " এই যে person ভেরিএবলটা লিখলেন সেইটা একবারই লিখলেন। পরবর্তীতে যদি আবার এই নামে ভ্যারিএবল লিখতে চান তখনই লেগে যাবে ঝগড়া মারামারি বলবে আমি তো আগে বসে আছি তুমি আবার আমার নামে আবার জায়গা দখল করছ। আর যদিও লিখে ফেলতে পারেন তখন নিজেই বিভ্রান্ত হয়ে যাবেন একই নামের দুইটা ভ্যারিএবল দেখে। আর এই সমস্যা গুলো থেকে বাঁচার জন্য ওষুধ কোম্পানি গুলো যেমন ক্যাপসুল করে মিক্স হওয়ার জামেলা সমাধান করে। টিক তেমন করে আমাদের ও করা লাগবে। যাতে করে আমাদের সকল ফাংশন ও ভ্যারিএবল অবাঞ্ছিত পরিবর্তন ও বিভ্রান্তিকরণ থেকে রক্ষা পাই।&#x20;

{% code title="উদাহরণঃ " lineNumbers="true" %}
```javascript
function Car(made_by, model) {
  // Private members
  let _made_by = made_by;
  let _model = model;

  // Public method to access private members
  this.getMaker = function() {
    return _made_by;
  };

  // Public method to access private members
  this.getModel = function() {
    return _model;
  };
}

const myCar = new Car("Toyota", "Camry");

console.log(myCar.getMaker()); // Output: Toyota
console.log(myCar.getModel()); // Output: Camry

```
{% endcode %}

কোড লক্ষ্য করলে দেখবেন আমি এইখানে Car নামে ক্লাস বানিয়েছি আর তার মধ্যে কিছু ফাংশন এবং কিছু ভেরিয়েবল লিখেছি এবং পরবর্তীতে তার একটা ইন্সটেন্স বানিয়েছি myCar নাম দিয়ে। তারপর আমি ঐ ক্লাসে অবজেক্ট বানানোর সময় তাতে দুইটা আরগুমেন্ট দিয়েছি "Toyota", "Camry" নামে প্রথম টা ছিল কে বানিয়েছে আর দ্বিতীয়টা ছিল গাড়ির মডেল। তার পরে আমি ঐ ইন্সটেন্সের উপর ভিত্তি করে দুইটা মেথড কল করেছি একটা হচ্ছে getMaker আরেকটা getModel ।

একটু ভাল করে লক্ষ্য করলেই বুঝতে পারবেন এইখানে যে প্রোপার্টি এবং মেথড গুলো আছে এগুলো এর সাথে অন্য কোন ফাংশনের বা প্রোপার্টির কোন সম্পর্ক নেই। কেউ চাইলেও বাইরে থেকে এখানে কোন পরিবর্ত্ন করতে পারবে না মানে getMaker কে পরিবর্তন করতে পারবে না।&#x20;

আশা করি বুঝতে পেরেছেন আর বুঝতে পারলেই আমার লিখা টা বৃথা হলো না&#x20;

এবার আসুন কিছু অনুশীলন দেই আপনি করে নিবেন টিক টাক মতো না করলে কিন্তু বঊ পাবেন না কেন পাবেন না পরে বলব।

**অনুশীলনঃ-**

১। আপনি আপনার নামে একটা ক্লাস বানাবেন আর তাতে আপনার বয়স, নাম ঠিকানা যুক্ত থাকবে এবং আপনার নাম ঠিকানা আর বয়স দেখাবেন কনসোল করে।

২। মনে করুন আপনি ব্যাংক একাউন্ট আছে এর জন্য আপনি একটা ক্লাস বানাবেন এবং এবং আপনার বর্তমান ব্যালেন্স , শেষ লেনদেন ও আপনার একাউন্ট নাম্বার দেখাবেন কনসোল করে ।&#x20;

৩। আপনি এখন একটা তাপমাত্রার ক্যালকুলেটর বানাবেন যেইটাতে ইনপুট হিসেবে থাকবে সেলসিয়াস তাপমাত্রা আপনাকে দেখাতে হবে ফারেনহাইটে এবং কেলভিনে।



