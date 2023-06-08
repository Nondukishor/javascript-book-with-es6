# ডেটা টাইপ

Data মানে কি বলেন তো ? Data মানে হলো তথ্য বা উপাত্ত । আর type মানে কি বলেন তো ? মানে হলো ধরন তার মানে আপনি বুঝেই গেছেন যে ডেটা টাইপ মানে হলো তথ্যের ধরণ । তাইলে ভাই আপনি তো শিখে ফেলেছেন ডাটা টাইপ। তাইলে এবার আমরা বলতে পারি জাভাস্ক্রিপ্টে ডাটা টাইপ হলো কোন ডাটা কি ধরনের হবে মানে কি টাইপের হবে সেটা বুঝায় সেটা হতে পারে কোন নাম্বার সেটা হতে পারে কোন দশমিক সংখ্যা সেটা হতে পারে কোন একটি ওয়ার্ড বা একগুচ্ছ লেখা ।

এখন আপনার মনে প্রশ্ন জাগতে পারে কেন ডাটা টাইপ গুলো কি কি একটু বলেন ?

আরে বলব না মানে ! বলার জন্যেই এই বই লেখা সো বলতে তো হবেই আমাকে । জাভাস্ক্রিপ্টে ডাটা টাইপ প্রধানত দুই প্রাকার

১। প্রিমিটিভ ডাটা টাইপ ।

২। ননপ্রিমিটিভ ডাটা টাইপ বার (রেফারেন্স ডাটা টাইপ।)

প্রিমিটিভ ডাটা টাইপ আবার।

* বুলিয়ান (Boolean)
* নাল (Null)
* আন্ডিফাইন্ড (Undefined)
* নাম্বার (Number)
* বিগ ইন্টিজার (BigInt)
* স্ট্রিং (String)
* সিম্বল (Symbol)

ননপ্রিমিটিভ বা রেফারেন্স ডাটা টাইপঃ

* অ্যারে
* অব্জেক্ট

**প্রিমিটিভ ডাটা টাইপঃ-** প্রিমিটিভ ডাটা immutable(অপরিবর্তনীয়) ডাটা টাইপ হিসাবে পরিচিত। কারন এই ডাটাটাইপ একবার তৈরী হয়ে গেলে পরিবর্তন করা যায় না তাই একে অপরিবর্তনীয় ডাটাটাইপ বলে । তো আসুন এখন সেই অপরিবর্তন করার কথা টা প্রামান করতে পারি কিনা ।

মনে করে আপানার কাছে একটা দশ টাকার নোট আছে আর আপনি একটা পটেটো চিপস খাবেন । এবং চিপসের গায়ে দশ টাকা লেখা আছে এখন যদি আপনি বার বার চেষ্টা ও করেন চিপসের দাম কমবে না মানে অপরিবর্তনীয় । তবে আসল কথা তো সেটা না এখানে আসল কথা হলো বস্তুটার টাইপ হলো চিপস আর আপনি চাইলেও এটারে নুডুলস বানাইতে পারবেন না যদি ও কোম্পানী চাইলে চিপ্সের দাম বাড়াইতে পারে কিন্তু সেটাকে নুডুলস বলতে পারবে না । তার মানে মাথায় রাখেন ভ্যালু পরিবর্তন করতে পারেন আপনি কিন্তু টাইপ না জদিও তাও করা যায় সেটার জন্য মেথড ও আছে বিল্ডিইন ।

আশা করি বুঝতে পেরেছেন আমার কথা গুলো না বুঝে থাকলে আমার মেইল আছে মেইলে টুং করে একটা মেইল করে দেন আমি চেষ্টা করব আপনাকে যতটুকই পারি আরেকবার বুঝাতে তবে মনে রখাবেন আমায় কিন্তু চা খাওয়াতে হবে এর জন্য আমি ফ্রি উপকার করব না ।

এতক্ষন আমরা শুধু গল্প করে গেছি এখন একটু প্রোগ্রাম করে বুঝে নেই বিষয়টা

```javascript
const chips ="10";
const tentaka = 10;
console.log(chips===tentaka)

```

Output:

```javascript
false 
```

কি হলো? আপনি তো চিন্তা করছেন চিপস তো দশ টাকা আছে আমার কাছে দশ টাকা তাইলে তো সমান ? আরে বাবা আপনি আবার গুলাইছেন আর গুলায় পুরো দই হয়ে গেছেন আমি বুজতে পেরেছি আপনি আবার দু ' টার ভ্যালু চিন্তা করতেছেন আরে ভাই ভ্যালু না ! ভ্যালু না ! টাইপ চিন্তা করেন চিপস মানে চিপস টাকা মানে টাকা পানির মতো পরিষ্কার একদম । আমি জানি আপনি আবার মনে মনে বলতেছেন ভাই কেম্নে ? তো আসেন আরেকটু ক্লিয়ার করে দেই।

```javascript
console.log( typeof chips );
> string
console.log( typeof tentaka);
> number 
```

তাহলে আশা করি আপনি বুঝতে পেরেছেন প্রিমিটিভ ডাটাটাইপ কাকে বলে এবং সেটা কেন পরিবর্তনযোগ্য নয়।

এবার আসুন আমরা আরেকটু এইডাটা টাইপ গুলো নিয়ে আলোচনা করে নেই















স্ট্রিং এর প্রোপার্টিঃ-

```
String length
String.prototype
```

বিল্ডি ইন মেথডঃ-

```
String.prototype.repeat()
String.prototype.replace()
String.prototype.search()
String.prototype.slice()
String.prototype.split()
String.prototype.startsWith()
String.prototype.substring()
String.prototype.toLocaleLowerCase()
String.prototype.toLocaleUpperCase()
String.prototype.toLowerCase()
String.prototype.toString()
String.prototype.toUpperCase()
String.prototype.trim()
String.prototype.trimEnd()
String.prototype.trimStart()
String.prototype.valueOf()
String.prototype[@@iterator]()
String.raw()
```

সিম্বলের বিল্ডি ইন প্রোপার্টি গুলো হলোঃ-

```javascript
Symbol.asyncIterator
Symbol.hasInstance
Symbol.isConcatSpreadable
Symbol.iterator
Symbol.match
Symbol.matchAll
Symbol.prototype
Symbol.prototype.description
Symbol.replace
Symbol.search
Symbol.species
Symbol.split
Symbol.toPrimitive
Symbol.toStringTag
Symbol.unscopables
```

বিল্ড ইন ফাংশন সমূহঃ

```javascript
Symbol.for()
Symbol.keyFor()
Symbol.prototype.toSource()
Symbol.prototype.toString()
Symbol.prototype.valueOf()
Symbol.prototype[@@toPrimitive]
```
