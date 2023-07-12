# প্রিমিটিভ ডাটা টাইপ

**প্রিমিটিভ ডাটা টাইপঃ-** প্রিমিটিভ ডাটা immutable(অপরিবর্তনীয়) ডাটা টাইপ হিসাবে পরিচিত। কারন এই ডাটাটাইপ একবার তৈরী হয়ে গেলে পরিবর্তন করা যায় না তাই একে অপরিবর্তনীয় ডাটাটাইপ বলে । তো আসুন এখন সেই অপরিবর্তন করার কথা টা প্রামান করতে পারি কিনা ।

মনে করে আপানার কাছে একটা দশ টাকার নোট আছে আর আপনি একটা পটেটো চিপস খাবেন । এখন চিপস নেওয়ার পরে আপনার মনে হলো আপনার আসলে বার্গার খেতে ইচ্ছা করছিল এখন আপনি যতই চেষ্টা করেন এর ভিতরে থাকা জিনিস পত্র বার্গার বানাতে পারবেন না। তবে আপনি চাইলে দোকানদারের সাথে কথা বলে পাল্টায় নিতে পারেন যে ভাই আমার বার্গার লাগবে। তার মানে মাথায় রাখেন আপনি পুরো টা পরিবর্তন করতে পারেন কিন্তু কিছু সংখ্যক না। কিন্তু টাইপ না যদিও তাও করা যায় সেটার জন্য মেথড ও আছে বিল্ডিইন ।

আশা করি বুঝতে পেরেছেন আমার কথা গুলো না বুঝে থাকলে আমার মেইল আছে মেইলে টুং করে একটা মেইল করে দেন আমি চেষ্টা করব আপনাকে যতটুকই পারি আরেকবার বুঝাতে তবে মনে রখাবেন আমায় কিন্তু চা খাওয়াতে হবে এর জন্য আমি ফ্রি উপকার করব না ।

এতক্ষন আমরা শুধু গল্প করে গেছি এখন একটু প্রোগ্রাম করে বুঝে নেই বিষয়টা

```javascript
const chips ="Potato";
chips[0]="B"
chips[1]="u"
chips[2]="r"
chips[3]="g"
chips[4]="e"
chips[5]="r"
console.log(chips)
```

Output:

```javascript
Potato 
```

কি হলো? আপনি তো Potato কে  Burger  বানাইতে চেয়েছিলেন কিন্তু হলো না কেন? এইটার উত্তর আগেই দেওয়া হয়েছে কারন এইটা অপরিবর্তনীয় ।&#x20;

```javascript
console.log( typeof chips );
> string
```

তাহলে আশা করি আপনি বুঝতে পেরেছেন প্রিমিটিভ ডাটাটাইপ কাকে বলে এবং সেটা কেন পরিবর্তনযোগ্য নয়।