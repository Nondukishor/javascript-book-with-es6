# 📿 পুনারাবৃত্তি (Iteration)

জাভাস্ক্রিপ্টে অনেক গুলো বিল্ড ইন উচ্চ আদেশ  (Higher Order Function) ফাংশন আছে । যেমনঃ forEach, map, filter, find, reduce এবং every. পুনারাবৃত্তি (Iteration) বিষয় টা খুবই মিল মিল বিষয় লুপের সাথে। লুপ হচ্ছে একটি নির্দিষ্ট কন্ট্রোল কাঠামো যেইটা  একটি নির্দিষ্ট ব্লককে নির্দিষ্ট শর্ত এর ভিত্তিতে পুনরাবৃতি করে। আর পুনারাবৃত্তি (Iteration) হচ্ছে একটি বিন্যাস(Array) এর উপর ভিত্তি করে বা কিছু উপদানের উপর ভিত্তি করে সেইটা কে একে একে দেখানো বা ব্লক উপদান গুলোর মধ্য দিয়ে যাওয়া ।&#x20;

জানি উপরের বিষয় গুলো বুঝতে একটু কষ্ট হয়েছে অনেকের কারণ বিষয় অত সহজ না। আমি এই বিষয় গুলো আরো বিস্তারিত উচ্চ আদেশ(Higher Order Function) আধ্যায়ে আলোচনা করেছি। পড়তে থাকুন আস্তে আস্তে বুঝে যাবেন আমাদের কোন তারা নেই ।&#x20;

এখন আসেন জাভাস্ক্রিপ্টের পুনারাবৃত্তি (Iteration) নিয়ে কয়েকটা উদাহরন দেখি।

ধরুন আপনার কাছে একটা বাড়ির দৈনিক খরচের তালিকা আছে। নিচের মত করে&#x20;

```javascript
const dailyHomeCosts = [
  50, 60, 45, 55, 70, 65, 80, 75, 60, 55,
  70, 75, 65, 80, 90, 85, 70, 55, 75, 80,
  60, 65, 70, 75, 55, 50, 65, 80, 75, 60
];

```

এখন আপনার এইখান থেকে বের করতে হবে আপনি ৮০ টাকা বা তার উপরে বাজার করেছেন সেই খরচ গুলো&#x20;

চলুন বেশি দেরি না করে বের করে ফেলি।&#x20;

```javascript
const highestCost = dailyHomeCosts.filter((cost)=>cost>=80)
console.log(highestCost )
```

Output:

```
[ 80, 80, 90, 85, 80, 80 ]
```

ব্যাস সে কিন্তু আপনাকে সাথে সাথে ৮০ টাকা বা তার উপরে বাজার বাজার খরচ গুলো দিয়ে দিবে।&#x20;

চলুন এবার আমরা এই ফাংশন গুলোর ব্যাবহার দেখব।

প্রথমেই আমরা কিছু নাম্বার নিয়ে নেইঃ

```javascript
const numbers = [1,2,3,4,5,6,7,8]
```

**forEach**  একটা কলব্যাক ফাংশন নেয় এবং সেই ফাংশন  আসলে অ্যারে এর প্রতিটা ইলিমেন্টের মধ্য দিয়ে যাবে কিন্তু কোন কিছু আপনাকে ফেরত বা রিটার্ন দিবে না। মানে হলো সে আপনাকে নতুন কোন অ্যারে দিবে না।&#x20;

<pre class="language-javascript"><code class="lang-javascript"><strong>numbers.forEach(number => {
</strong>  console.log(number * 2);
});

</code></pre>

**map:** একটা কলব্যাক ফাংশন নেয় এবং সেই আসলে অ্যারে  এর প্রতিটা ইলিমেন্টের মধ্য দিয়ে যাবে এবং আপনি যে  অ্যারেটা দিয়েছেন সেইটার উপর ভিত্তি করে আপনাকে একটা নতুন অ্যারে ফেরত দিবে। মনে রাখা শ্রেয় যে আপনাকে যে অ্যারে ফেরত দিবে সেইটার length  আর  map কে দেওয়া অ্যারে  এর length কিন্তু সমান হবে।&#x20;

```javascript
const doubledNumbers = numbers.map(number => number * 2);
console.log(doubledNumbers); 
// Output: [2, 4, 6, 8, 10]
```

**filter:**

```javascript
const evenNumbers = numbers.filter(number => number % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```

**find:**&#x20;

```javascript
const firstEven = numbers.find(number => number % 2 === 0);
console.log(firstEven); // Output: 2
```

**reduce:**

```javascript
const sum = numbers.reduce((accumulator, currentNumber) => accumulator + currentNumber, 0);
console.log(sum); // Output: 15
```

**every:**

```javascript
const allEven = numbers.every(number => number % 2 === 0);
console.log(allEven); // Output: true
```

**some:**

```javascript
const hasEven = numbers.some(number => number % 2 === 0);
console.log(hasEven); // Output: true
```

**reduceRight:**

```javascript
const result = numbers.reduceRight((acc, num) => acc - num, 0);
console.log(result); // Output: -2 (0 - 4 - 3 - 2 - 1)
```
