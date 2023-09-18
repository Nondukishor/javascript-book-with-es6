# Async এবং await (Async & Await)

Async শব্দের অর্থ হলো অসমনিয়ত। মানে হলো আপনি এমন কোন কাজ করতে চাইছেন যেইটা আসলে একটার পর একটা হবে না বা সিরিয়ালি হবে না। তাহলে কেমন করে হবে?&#x20;

তাহলে বিষয়টা ঘটনা বলি, ধরুন আপনি কোন একটা কুরিয়ার সার্ভিস কোম্পানি এর মালিক।ধরে নিলাম আপনার কোম্পানির নাম হচ্ছে **আত্মবিশ্বাস** এখন আপনি অনেকের কাজ থেকে পন্য নেন এবং তাদের গন্তব্য স্থলে পৌছে দেন।&#x20;

&#x20;ধরুন **দিলদার** নামে একজন ব্যাক্তি **১১ তারিখ সকাল ১০ঃ০০ টায়** পন্য কুরিয়ার সার্ভিসে জমা দিয়েছে যার গন্তব্যস্থল হচ্ছে **চট্টগ্রামের কাপ্তাই** এলাকা। **বাপ্পারাজ** নামে আরেকজন তার বউয়ের জন্য শাড়ি পাঠিয়েছে।যার গন্তব্যস্থল হচ্ছে **রাঙ্গামাটি এলাকা।** জমা দেওয়ার সময় ছিল **১১ তারিখ সকাল ৯ঃ০০ টা** ।**জসিম** নামে আরেক ব্যাক্তি তার বউয়ের জন্য সেলাই মেশিন পাঠিয়েছেন। যার গন্তব্যস্থল হচ্ছে  চট্টগ্রামের **বদ্দার হাট** এলাকা। জমা দেওয়ার সময় ছিল একই তারিখে সকাল ১২ঃ০০টা । এখন **আত্মবিশ্বাস** কোম্পানির লোকেশন  হচ্ছে ঢাকা **গুলশান-১** । আপনি যখন পন্য নিয়ে রওনা দিলেন অবশ্যই যার গন্তব্যস্থল আগে অবশ্যই তার পণ্য ডেলিভারি দিবেন ।তার মানে বিষয়টা কিন্তু অন্য রকম হয়ে গেল যে আগে পণ্য জমা দিয়েছে তার পরিবর্তে যার গন্তব্য আগে সে পণ্য পাচ্ছে। আসুন টেবিলের মধ্যমে বিষয়টা আরেকটু বিশ্লেষণ করে দেখি।&#x20;

<table data-full-width="false"><thead><tr><th>আপানার কোম্পানি লোকেশন</th><th>গন্তব্য দূরত্ব</th><th>গন্তব্য এর নাম</th></tr></thead><tbody><tr><td><strong>আত্মবিশ্বাস গুলশান-১</strong></td><td>৩০১ কিঃ মিঃ </td><td><strong>কাপ্তাই(দিলদার)</strong></td></tr><tr><td><strong>আত্মবিশ্বাস গুলশান-১</strong></td><td>৩০৬ কিঃ মিঃ </td><td><strong>রাঙ্গামাটি(বাপ্পারাজ)</strong></td></tr><tr><td><strong>আত্মবিশ্বাস গুলশান-১</strong></td><td>২৫২ কিঃ মিঃ</td><td><strong>বদ্দার হাট(জসিম)</strong></td></tr></tbody></table>

এখন আপনি আপনি আশা করি বুঝে নিয়েছেন যে কার টা আগে ডেলিভারি হবে। তো উত্তর হচ্ছে জসিম। কেন? কারণ জসিমের বসার দূরত্ব কম তাই জসিম আগে পাবেন। তারপর দিলদার সাহেবের তারপর বাপ্পারাজ । আর এই যে পুরো বিষয় টা এইটায় হচ্ছে Async বা Asynchronous ।

এবার আসি আসল কথায় আমারা এর আগেই জেনেছি প্রমিস নামে এমন একটা জিনিস আগে থেকেই আছে তাহলে আমারা Async লিখতে যাচ্ছি কেন?

উত্তর হচ্ছে আমরা আসলে প্রমিসের যে সিন্ট্যাক্স সেটাকে ছোট করে লেখার জন্য এমন টা করেছি বা আমাদের কোন ফাংশনে যাতে আমরা খুব সহজে প্রমিস বিষয় টা যুক্ত করতে পারি তার জন্য এমন টা করছি।&#x20;

তাহলে এবার একটা উদাহরণ দেখে নিই কিভাবে লিখে Async ফাংশন।

{% code title="async-with-regular.js" overflow="wrap" lineNumbers="true" %}
```javascript
async function regularFunction() {
 //statements
}

```
{% endcode %}

রেগুলার ফাংশনের সাথে যদি আমরা async লিখি সে ক্ষেত্রে প্রথমে async কী-ওয়ার্ড এরপর ফাংশন কী-ওয়ার্ড এবং এর পরে ফাংশনের নাম লিখতে হবে। এর পরে আপনার যে statement আছে সেগুলো {} প্রথম বন্ধনী এর মাঝে লিখতে হবে। উপরের কোডটি লক্ষ্য করলে বুঝতে পারবেন।

{% code title="async-with-arrow.js" lineNumbers="true" %}
```javascript
const arrowAsyncFunction = async () => {
  //statements
};

```
{% endcode %}

অ্যারো ফাংশনের সাথে যদি আমরা async লিখি সে ক্ষেত্রে প্রথমে let , const অথবা var কী-ওয়ার্ড লিখতে হবে । এরপরে ফাংশনের নাম লিখতে হবে। এরপরে (=)  assignment operator লিখতে হবে এবং পরে  async কী-ওয়ার্ড লিখতে হবে। এর পরে আপনার যে statement আছে সেগুলো {} প্রথম বন্ধনী এর মাঝে লিখতে হবে। উপরের কোডটি লক্ষ্য করলে বুঝতে পারবেন।

<pre class="language-javascript" data-title="async-with-class.js" data-overflow="wrap" data-line-numbers><code class="lang-javascript">class <a data-footnote-ref href="#user-content-fn-1">MyClass </a>{
  async classAsyncMethod() {
    //statements
  }
}

</code></pre>

ক্লাসের সাথে যদি async ফাংশন লিখি সে ক্ষেত্রে ক্লাস সিন্ট্যাক্স লিখে প্রথমে async কী-ওয়ার্ড লিখতে হবে এবং ফাংশনের নাম দিয়ে প্রথম বন্ধনী এর ভিতরে statements গুলো লিখতে হবে।&#x20;

এখন ফাংশন তো লিখে ফেললেন সেইটা কল করবেন কিভাবে তাও একটা ব্যাপার আছে। Async কল করার দুইটা উপায় আছে একটা হচ্ছে প্রমিসের মতো করে মেথড চেইনিং এবং আরেকটা হচ্ছে await চলুন দেখে নেই সেগুলো কিভাবে লিখে।

{% code overflow="wrap" lineNumbers="true" fullWidth="false" %}
```javascript
//with regular function
async function sum() {
  return 2+3
}

//With Promise syntax
sum.then(function(response){
  return response;
})

//with await syntax
const result = await sum()

// with arrow function
const sum = async ()=>{
 return 2+2;
}

//Promise syntax
sum.then(res=>console.log(res))

// await syntax 
const result = await sum()
console.log(result)


// with class member functions
class Mathmatic{
   async sum(){
     return 3+3;
   }
}

const math = Mathmatic()

//Promise syntax
math.sum().then(res=>console.log(res))

//await syntax
const result = await math.sum()
console.log(result)
```
{% endcode %}

এখন আসুন **await** নামে যে বিষয় টা আছে সেইটার একটু  গভীরে যায়। আসলে **await** বিষয় টা হচ্ছে, আমরা যে বিষয়টা **Asynchronous** ভাবে করতে চাইছিলাম সেইটা এখন **synchronous** ভাবে করতে চাইছি মানে আমি আবার এই কাজ টা জাভাস্ক্রিপ্টের ডিফল্ট ওয়েতে করতে চাইছি । আশা করি বুঝতে পেরেছেন। তাছাড়া আমরা যে প্রমিসে then চেইনিং মেথড এর ব্যাবহার করতাম তার কাজটাও কমিয়ে দিচ্ছে। await ব্যবহার করলে তখন আর এই চেইনিং মেথড এর দরকার পরে না তবে চেইনিং মেথড এর ইউস কেইস কিন্তু অন্য ব্যাপার কে বুজায়, বলে রাখলাম।&#x20;

#### সিকুয়েন্সিয়াল প্রসেসঃ&#x20;

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption><p>সিকুয়েন্সিয়াল প্রসেস</p></figcaption></figure>

উপরের চিত্র দেখে বুঝে যাবেন যে আমরা এইখানে একটা কাজের পর আরেকটা কাজ করছি এর এই বিষয়টা হচ্ছে সিকুয়েন্সিয়াল প্রসেস । যা জাভাস্ক্রিপ্ট ইন্টারপ্রেটারের মধ্যমে **Synchronous** ভাবে করে।&#x20;

**কনকারেন্সিঃ**&#x20;

কেমন হতো যদি একই সময়কে ভাগ করে নিতে পারতেন মানে একই সময় আপনি একের অধিক কাজ করে ফেলছেন। যেমন ধরুন আপনি মুভি দেখতে দেখতে পপকর্ন খাচ্ছেন আবার সাথে সাথে ফেইসবুকে নিউজ ফিডে আপনার বন্ধু বউয়ের সাথে কক্সবাজার গিয়ে ভিডিও দিয়েছে সেইটা দেখছেন তাই দেখে একই সাথে মন খারাপ করছেন। একটু ভেবে দেখুন তো কাজ গুলো কিন্তু আপনি একটা সময় কে ভাগ করে করে ফেলছেন মানে আপনি কোন একক সময়ে ভিন্ন ভিন্ন কাজ করে ফেলছেন যেইটা আপনি সিকুয়েন্সিয়েলি করতে গেলে টাইম বেশি লাগত।&#x20;

আশা করি বুঝে গেছেন কনকারেন্সি কি? কনকারেন্সি হচ্ছে কোন একক সময় ভিন্ন ভিন্ন কাজ কে একসাথে করার একটা উপায়।

{% code title="concurrency.js" overflow="wrap" lineNumbers="true" %}
```javascript
function routine(task, time) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(task);
    }, 1000 * time); // 1 sec = 1000 ms
  });
}

async function main() {
 
const task_list = ['Watching movie', 'Eating popcorn', 'Using Facebook to watch videos of friends and his wife's Cox's Bazar tour', 'Getting upset'];
  const times_for_task = [10, 30, 30, 30]
  const t0 = performance.now();
  const task_completed_log = await Promise.all(task_list.map((task, index)=> {
    return routine(task,times_for_task[index])
  }));
  console.log("task completed",task_completed_log)
  const t1 = performance.now();
  console.log(`Call to routine took ${(t1 - t0)/1000} sec. expected time was ${((10*1000)+(30*1000)+(30*1000)+(30*1000))/1000} sec`);
}
```
{% endcode %}

**output:**

```sh
task completed [
  'Watching movie',
  'Eating popcorn',
  'Using Facebook to watch videos of friends and his wife's Cox's Bazar tour',
  'Getting upset'
]
Call to routine took 30.023713645003735 sec. expected time was 100 sec
```

উপরের কোডটা লক্ষ্য করলে দেখবেন আমি আমি একসাথে অনেকগুলো টাস্ক কে এক্সিকিউশন প্রসেস এর মধ্য দিয়েছি। যেগুলো আসলে **Asynchronous** টাস্ক সে একটা টাস্কের জন্য এইখানে আমি টাইম বলে দিয়েছি যে একটা টাস্ক কয় মিনিট ধরে এক্সিকিউশন প্রক্রিয়ার মধ্য দিয়ে যাবে। টাইম অনুযায়ী আমার টাস্কটা গুলো কমপ্লিট হওয়ার কথা ছিল ১০০ সেঃ কিন্তু হায়! হায় ! একি হলো? তার আগেই আউটপুট পেয়ে গেলাম তাহলে আমি কি আসলে ভুল কোড লিখলাম ? উত্তর হচ্ছে না। আসুন বিষয়টা বুঝি। এইখানে আসলে যেইটা হয়েছে আমি যে টাইম টা দিয়েছি সেইটা কে সে অন্যভাবে এক্সিকিশন প্রসেসে নিয়ে গেছে।

সে এক সাথে সব টাস্কগুলো গুলোকে প্রসেসে নিয়ে গেছে&#x20;

আসুন চিত্র এর মধ্যমে দেখি।

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>concurrency</p></figcaption></figure>

বুঝতেই পারছেন প্রথম ১০ সেকেন্ডে প্রথম টাস্ক কমপ্লিট করে ফেলে এবং টিক বাকি টাস্ক গুলো কমপ্লিট হতে ২০ সেকেন্ড লাগবে কারণ ইতিমধ্যেই ১০ সেকেন্ড অতিক্রম হয়ে গেছে পরবর্তী টাস্ক গুলো ২০ সেকেন্ড ধরে এক্সকিউট হয়ে একই সময় পরে আউটপুট দিবে।&#x20;

> NOTE: কিছু সেকেন্ড যেগুলো বেশি দেখছেন এগুলো এই টাস্ক প্রসেস এর সাথে যে অন্যান্য কোড গুলো আছে সেগুলোর ও একটা প্রসেস টাইম আছে তাই ছাড়া **External Factors, Precision of Timing** এবং **Overhead** এই রকম অনেক গুলো ফ্যাক্টর আছে যার কারনে ৩০ সেকেন্ড থেকেও একটু বেশি সময় লেগেছে।

#### প্যরালাললিজমঃ

**Parallelism** বিষয়টা দেখতে অনেকটা কনকারেন্সি এর মতো দেখালেও কিন্তু একই না । নিচের চিত্রটি দেখুন।

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption><p>প্যারালাললিজম</p></figcaption></figure>

একটু যদি ভাল করে লক্ষ্য করুন দেখবেন বিষয় একটু ভিন্নতা আছে আগের উদাহরণে কিন্তু আপনি একটা করছিলেন সব কিন্তু আমাদের এবারের চিত্রে কিন্তু আলাদা আলাদা মানুষ কাজ গুলো সম্পন্ন করছে। এবং তারা তাদের মত করে আলাদা স্পেসে করছে এবং আলাদা টাইমে করছে। এইটাই মূলত **প্যারালালিজম** । একই সময়ে ভিন্ন ভিন্ন থ্রেড দ্বারা কাজ করায় হচ্ছে **প্যারালালিজম।** আসুন এবার কোড করে বিষয়টা বুঝে নেই।&#x20;

জাভাস্ক্রিপ্টে কিন্তু worker নামে একটা বিল্ডিইন এপি আই আছে যেইটা আমাদের একই সময় আলাদা আলাদা থ্রেড ব্যবহারের সুবিধা দিয়ে থাকে।

সেই Worker API দিয়ে আমরা প্রথমে কিছু Worker বানিয়ে নেই brush-worker.js, clean-worker.js, cook-worker.js, watch-tv-worker.js নামে নিচের মতো করে এবং কোড গুলো লিখে নেই।

{% code title="brush-worker.js" overflow="wrap" lineNumbers="true" %}
```javascript
self.onmessage = (event) => {
  console.log(`Brushing: ${event.data}`);
  self.postMessage('Finished brushing!');
};

```
{% endcode %}



{% code title="clean-worker.js" overflow="wrap" lineNumbers="true" %}
```javascript
self.onmessage = (event) => {
  console.log(`Cleaning the bedroom: ${event.data}`);
  self.postMessage('Finished cleaning the bedroom!');
};

```
{% endcode %}



{% code title="cook-worker.js" overflow="wrap" lineNumbers="true" %}
```
self.onmessage = (event) => {
  console.log(`Cooking breakfast: ${event.data}`);
  self.postMessage('Finished cooking breakfast!');
};

```
{% endcode %}



{% code title="watch-tv-worker.js" overflow="wrap" lineNumbers="true" %}
```javascript
self.onmessage = (event) => {
  console.log(`Watching TV: ${event.data}`);
  self.postMessage('Finished watching TV!');
};

```
{% endcode %}

আমাদের Worker বানানো শেষ হলে এখন আমরা সেই Worker  গুলো মেইন থ্রেডে নিয়ে আসব তাই প্রথমেই main.js নামে একটা ফাইল বানাব এবং নিচে লেখা কোডের মতো করে Worker গুলো ইমপ্লিমেন্ট করে নিব। করা&#x20;

করা শেষ হলে এখন আমরা Worker এ আমাদের মেইন থ্রেড থেকে মেসেজ পাঠাবো ৩, ৭ , ১১ এবং ১৫ নাম্বার লাইনের মতো করে। এবার আমরা সে আমাদের Worker  এর সাথে যোগাযোগ করে আমাদের যে ডাটা দিবে সেই ডাটা আমরা রিসিভ করব। ১৮,২২, ২৬ এবং ৩০ নাম্বার লাইনের মতো করে। ব্যাস আমাদের কাজ শেষ। ওয়ার্কার গুলো তাদের মতো করে কমিউনিকেশন করে নিবে এবং ডাটা দিয়ে দিবে কোন সমস্যা ছাড়াই। Worker এপি আই নিয়ে আমি আরো বিস্তারিত লিখেছি ওয়েব এপি আই অধ্যায়ে তাই এইখানে আর বেশি বললাম না।&#x20;

{% code title="main.js" overflow="wrap" lineNumbers="true" %}
```javascript
// Create a worker for brushing
const brushWorker = new Worker('brush-worker.js');
brushWorker.postMessage('Start brushing!');

// Create a worker for cleaning the bedroom
const cleanWorker = new Worker('clean-worker.js');
cleanWorker.postMessage('Start cleaning the bedroom!');

// Create a worker for cooking breakfast
const cookWorker = new Worker('cook-worker.js');
cookWorker.postMessage('Start cooking breakfast!');

// Create a worker for watching the news on TV
const watchTvWorker = new Worker('watch-tv-worker.js');
watchTvWorker.postMessage('Start watching TV!');

// Listen for messages from workers
brushWorker.onmessage = (event) => {
  console.log(`You: ${event.data}`);
};

cleanWorker.onmessage = (event) => {
  console.log(`Your wife: ${event.data}`);
};

cookWorker.onmessage = (event) => {
  console.log(`Your mom: ${event.data}`);
};

watchTvWorker.onmessage = (event) => {
  console.log(`Your father: ${event.data}`);
};

```
{% endcode %}



[^1]: 
