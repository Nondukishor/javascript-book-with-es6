# সিম্বল (Symbol)

**সিম্বলঃ** সিম্বল জাভাস্ক্রিপ্টের একটি বিশেষ ডাটাস্ট্রাকচার ও বিল্ডিন অবজেক্ট । যেইটা আপনাকে গ্যারান্টি দেয় যে সে একটি ইউনিক বা স্বতন্ত্র অবজেক্ট ।

```javascript
var sym1 = Symbol();
var sym2 = Symbol('this is a symbol');
var sym3 = Symbol('this is another symbol');
```

### সিম্বল এর বৈশিষ্ট্যঃ

* **অপরিবর্তিনীয়ঃ** একবার তৈরি হলে একটি Symbol এর মান পরিবর্তন করা যায় না।
* **বর্ণনা যুক্ত করণঃ**  সিম্বলে চাইলে বর্নণা যুক্ত করা যায় যা ঐ কে বোধগম্য করে তুলে এবং ডিবাগিং এও সুবিধা প্রাধান করে থাকে।&#x20;
* **স্বতন্ত্রঃ**  প্রতিবার Symbol() কল করলে একটি নতুন,  স্বতন্ত্র Symbol তৈরি হয়।
* **অনুসন্ধানযোগ্য নয়ঃ** সিম্বল লুপ করে অনুসন্ধান করা যায় না যদি অনুসন্ধান করা ধরকার পরে থাহলে এর কিছু নিজস্ব লুপ বা ইটারেটর মেথড আছে সেগুলো দিয়ে করা লাগে।&#x20;

