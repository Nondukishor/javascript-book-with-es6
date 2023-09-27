# 📿 পুনারাবৃত্তি (Iteration)

জাভাস্ক্রিপ্টে অনেক গুলো বিল্ড ইন উচ্চ আদেশ  (Higher Order Function) ফাংশন আছে । যেমনঃ forEach, map, filter, find, reduce এবং every. পুনারাবৃত্তি (Iteration) বিষয়টা খুবই মিল মিল বিষয় লুপের সাথে। লুপ হচ্ছে একটি নির্দিষ্ট কন্ট্রোল কাঠামো যেইটা  একটি নির্দিষ্ট ব্লককে নির্দিষ্ট শর্ত এর ভিত্তিতে পুনরাবৃতি করে। আর পুনারাবৃত্তি (Iteration) হচ্ছে একটি বিন্যাস(Array) এর উপর ভিত্তি করে বা কিছু উপদানের উপর ভিত্তি করে সেইটাকে একে একে দেখানো বা ব্লক উপদান গুলোর মধ্য দিয়ে যাওয়া ।&#x20;

জানি উপরের বিষয় গুলো বুঝতে একটু কষ্ট হয়েছে অনেকের কারণ বিষয়টা অত সহজ না। আমি এই বিষয় গুলো আরো বিস্তারিত উচ্চ আদেশ(Higher Order Function) আধ্যায়ে আলোচনা করেছি। পড়তে থাকুন আস্তে আস্তে বুঝে যাবেন আমাদের কোন তারা নেই ।&#x20;

এখন আসেন জাভাস্ক্রিপ্টের পুনারাবৃত্তি (Iteration) নিয়ে কয়েকটা উদাহরন দেখি।

ধরুন আপনার কাছে একটা বাড়ির দৈনিক খরচের তালিকা আছে। নিচের মত করে ।&#x20;

```javascript
const dailyHomeCosts = [
  50, 60, 45, 55, 70, 65, 80, 75, 60, 55,
  70, 75, 65, 80, 90, 85, 70, 55, 75, 80,
  60, 65, 70, 75, 55, 50, 65, 80, 75, 60
];

```

এখন আপনার এইখান থেকে বের করতে হবে আপনি ৮০ টাকা বা তার উপরে বাজার করেছেন সেই খরচ গুলো&#x20;

চলুন বেশি দেরি না করে বের করে ফেলি।&#x20;

{% code title="উদাহরণঃ " lineNumbers="true" %}
```javascript
const highestCost = dailyHomeCosts.filter((cost)=>cost>=80)
console.log(highestCost )
```
{% endcode %}

{% code title="Output:" %}
```
[ 80, 80, 90, 85, 80, 80 ]
```
{% endcode %}

ব্যাস সে কিন্তু আপনাকে সাথে সাথে ৮০ টাকা বা তার উপরে বাজার বাজার খরচ গুলো দিয়ে দিবে।&#x20;

চলুন এবার আমরা এই ফাংশন গুলোর ব্যাবহার দেখব। প্রথমেই আমরা কিছু নাম্বার নিয়ে নেইঃ

```javascript
const numbers = [1,2,3,4,5,6,7,8]
```

**forEach:** একটা কলব্যাক ফাংশন নেয় এবং সেই ফাংশন  আসলে অ্যারে এর প্রতিটা ইলিমেন্টের মধ্য দিয়ে যাবে কিন্তু কোন কিছু আপনাকে ফেরত বা রিটার্ন দিবে না। মানে হলো সে আপনাকে নতুন কোন অ্যারে দিবে না।&#x20;

{% code title="সিনট্যাক্সঃ " lineNumbers="true" %}
```javascript
originalArray.forEach((currentValue, index, array) => {
  // perform some operation using currentValue
});
```
{% endcode %}

<pre class="language-javascript" data-title="উদাহরণঃ" data-line-numbers><code class="lang-javascript"><strong>numbers.forEach(number => {
</strong>  console.log(number * 2);
});
</code></pre>

**map:** একটা কলব্যাক ফাংশন নেয় এবং সেই আসলে অ্যারে  এর প্রতিটা ইলিমেন্টের মধ্য দিয়ে যাবে এবং আপনি যে  অ্যারেটা দিয়েছেন সেইটার উপর ভিত্তি করে আপনাকে একটা নতুন অ্যারে ফেরত দিবে। মনে রাখা শ্রেয় যে আপনাকে যে অ্যারে ফেরত দিবে সেইটার length  আর  map কে দেওয়া অ্যারে  এর length কিন্তু সমান হবে। &#x20;

{% code title="সিনট্যাক্সঃ" lineNumbers="true" %}
```javascript
const newArray = originalArray.map((currentValue, index, array) => {
  // return transformed value based on currentValue
});
```
{% endcode %}

{% code title="উদাহরনঃ " lineNumbers="true" %}
```javascript
const doubledNumbers = numbers.map(number => number * 2);
console.log(doubledNumbers); 
// Output: [2, 4, 6, 8, 10]
```
{% endcode %}

**filter:**  এইটা ও একটা কলব্যাক ফাংশন নিবে এবং আপানার ফাংশনের ভ্যালু যে সমস্ত স্টেটমেন্টের জন্য সত্য হবে সেসকল উপদানের জন্য নতুন একটি অ্যারে ফেরত বা রিটার্ন দিবে।&#x20;

{% code title="সিনট্যাক্সঃ" lineNumbers="true" %}
```javascript
const newArray = originalArray.filter((currentValue, index, array) => {
  // return true or false based on some condition using currentValue
});

```
{% endcode %}

{% code title="উদাহরনঃ" lineNumbers="true" %}
```javascript
const evenNumbers = numbers.filter(number => number % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```
{% endcode %}

**find:**  এইটা আগের মত করে একটা কলব্যাক ফাংশন নিবে কিন্তু যে স্টেটমেন্টের জন্য সত্য শুধু মাত্র সেই ভ্যালু টা ফেরত দিবে বা রির্টান করবে

{% code title="সিনট্যাক্সঃ" %}
```javascript
const result = originalArray.find((currentValue, index, array) => {
  // return true or false based on some condition using currentValue
});

```
{% endcode %}

{% code title="উদাহরনঃ " lineNumbers="true" %}
```javascript
const firstEven = numbers.find(number => number % 2 === 0);
console.log(firstEven); // Output: 2
```
{% endcode %}

**reduce:** এইটা দুইটা প্যারামিটার নেয় প্রথম প্যারামিটার হিসেবে reduce একটা কলব্যাক ফাংশন নেয় এবং ঐ কলব্যাক ফাংশন দুইটা প্যারামিটার নেয় আর একটা হচ্ছে accumulator আরেকটা হচ্ছে currentvalue আর ২য় প্যারামিটার টা হচ্ছে initialvalue ।&#x20;

{% code title="সিনট্যাক্সঃ" overflow="wrap" lineNumbers="true" %}
```javascript
const result = originalArray.reduce((accumulator, currentValue, index, array) => {
  // return updated accumulator value based on currentValue
}, initialValue);

```
{% endcode %}

{% code title="উদাহরনঃ " %}
```javascript
const sum = numbers.reduce((accumulator, currentNumber) =>{
   return accumulator + currentNumber, 0);
}
console.log(sum); // Output: 15
```
{% endcode %}

**every:** এইটা একটা কলব্যাক ফাংশন নেয় এবং ঐ ফাংশনের স্টেটমেন্টে লিখা প্রত্যকটি উপদানের জন্য যদি সত্য হয় তাহলে every true রিটার্ন করে অথবা false রিটার্ন করে ।&#x20;

{% code title="সিনট্যাক্সঃ" lineNumbers="true" %}
```javascript
const result = originalArray.every((currentValue, index, array) => {
  // return true or false based on some condition using currentValue
});

```
{% endcode %}

{% code title="উদাহরণঃ " overflow="wrap" lineNumbers="true" %}
```javascript
const allEven = numbers.every(number => number % 2 === 0);
console.log(allEven); // Output: true
```
{% endcode %}

**some:** একটা কলব্যাক ফাংশন নেই এবং ঐ ফাংশনে লিখা কোন একটা স্টেটমেন্ট ও যদি সত্য হয় তাহলে true রিটার্ন করে নতুবা false রির্টান করে।&#x20;

{% code title="সিনট্যাক্সঃ" lineNumbers="true" %}
```javascript
const result = originalArray.some((currentValue, index, array) => {
  // return true or false based on some condition using currentValue
});

```
{% endcode %}

{% code title="উদাহরনঃ" lineNumbers="true" %}
```javascript
const hasEven = numbers.some(number => number % 2 === 0);
console.log(hasEven); // Output: true
```
{% endcode %}

**reduceRight:**  এইটা একটা কলব্যাক ফাংশন নেই এবং reduce টিক উল্টো কাজ করে মানে সে অ্যারে এর শেষ থাকে কাজ করে এইখানে accumulator শেষ থেকে এবং ভ্যালু হোল্ড করে&#x20;

{% code title="সিনট্যাক্সঃ" overflow="wrap" lineNumbers="true" %}
```javascript
const result = originalArray.reduceRight((accumulator, currentValue, index, array) => {
  // return updated accumulator value based on currentValue
}, initialValue);

```
{% endcode %}

{% code title="উদাহরণ " lineNumbers="true" %}
```javascript
const result = numbers.reduceRight((acc, num) => acc - num, 0);
console.log(result); // Output: -2 (0 - 4 - 3 - 2 - 1)
```
{% endcode %}
