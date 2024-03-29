# কারিং ফাংশন (Currying function)

কারিং (currying) হল ফাংশনাল প্রোগ্রামিং এবং জাভাস্ক্রিপ্টের একটি কৌশল যা একাধিক আর্গুমেন্ট গ্রহণ করে এমন একটি ফাংশনকে একগুচ্ছ ফাংশনে রূপান্তর করে, যার প্রত্যেকটি একটি করে আর্গুমেন্ট গ্রহণ করে।&#x20;

নিচের কোডটা একটু লক্ষ্য করুনঃ-

{% code title="currying-fn.js" overflow="wrap" lineNumbers="true" %}
```javascript
function add(x) {
  return function(y) {
    return x + y;
  };
}

// Usage
const addFive = add(5); // partially applying the function
console.log(addFive(3)); // Outputs 8
```
{% endcode %}

> কোডটা বুঝে নেই কি করেছি?
>
> প্রথমে একটা ফাংশন লিখেছি add নামে লাইন নাম্বার ১ - ৫ মতো করে এবং ফাংশনটা একটা আরগুমেন্ট নিচ্ছে এবং রেজাল্ট হিসেবে একটা নাম বিহীন বা anonymous ফাংশন রিটার্ন করছে  লাইন নাম্বার ২-৪ এর মতো করে। সেই anonymous ফাংশনটা add ফাংশনে আমরা যে আরগুমেন্ট পাস করেছিলাম সেইটা নিয়ে তার আরগুমেন্টের সাথে যোগ করে নিচ্ছে লাইন নাম্বার ৩ এর মতো করে এবং রেজাল্টটা রিটার্ন করে দিচ্ছে।

#### কারিং ফাংশন কেন নাম করিং করা হলো ?

আসলে কারিং ফাংশন যে শুধু জাভাস্কিপ্টের একটা টেকনিক এইটা কিন্তু না একটা মূলত ফানশনাল প্রোগ্রামিং এর কনসেপ্ট। বিখ্যাত মার্কিন যুক্তরাষ্টিয় গণিতবিদ ও যুক্তিবিদ স্যার **Haskell Curry** এর নাম অনুসারে এর নাম করিন করা হয় কারিং ফাংশন। মুলত এই ফাংশন জনপ্রিয় হয়েছিল সংমিশ্রণমূলক যুক্তির জন্য। তবে নামটি যে স্যার **Haskell Curry** রেখেছিলেন তা কিন্তু না । এই নামটা রেখেছিলেন বিখ্যাত কম্পিউটার বিজ্ঞানী স্যার **Christopher Strachey**। স্যার **Christopher** ছিলেন একজন অত্যান্ত মেধাবী programming language  এবং formal semantics বিষেশজ্ঞ ছিলেন। তিনিই মূলত স্যার **Haskell Curry** গাণিতিক বিষয় গুলো প্রোগ্রামিং ল্যাঙ্গুয়েজে যুক্ত করেন। তবে এইখানেও একটু বিতর্ক আছে স্যার **Moses Schönfinkel** দাবী করে তার এই আইডিয়া স্যার **Haskell Curry**  এর আরো ৬ বছর আগে ছিলো এবং Schönfinkelisation নামে সেইটার পরচিতি ছিল। যাহোক আমরা ঐ দিকে আর না যায়। আপনাদের আরো এই বিষয়ে জানতে ইচ্ছা হলে গুগল করে জানতে পারেন। &#x20;

চলুন আরেকটা কোড দেখে নেই।

{% code title="compose.js" overflow="wrap" lineNumbers="true" %}
```javascript
function compose(f, g) {
  return function (x) {
    return f(g(x));
  };
}

const double = (x) => x * 2;
const square = (x) => x ** 2;

const doubleThenSquare = compose(square, double);
console.log(doubleThenSquare(3)); // Outputs 36

```
{% endcode %}

