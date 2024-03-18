# ওয়ার্কার এপি আই (Workers API)

### Worker API কী?&#x20;

Worker API জাভাস্ক্রিপ্টের একটি বিল্ড ইন API যেইটা আপনার কোডকে ব্যাকগ্রাউন্ডে রান করতে সহযোগিতা করে থাকে। এক কথাইয় যদি বলি জাভাস্ক্রিপ্টকে মাল্টিথ্রেডিং সুবিধা দিয়ে থাকে। যা মুলত মেইন থ্রেডের বাইরে গিয়ে কাজ করে এবং মেইন থ্রেডকে ইফেক্ট না করে কোড এক্সিকিউট করে থাকে।&#x20;

### কখন আমরা Worker API ব্যবহার করব?

যখন আমাদের কাছে যদি এমন কোন কোড বা সমস্যা আসে যা অনেক সময় নিয়ে এক্সিকিউট হয় তাহলে আমাদের Worker API  ব্যবহার করতে হবে। উদাহরণ দিয়ে যদি বলিঃ- ধরে নিলাম আপনার কাছে ১০০০০০ ডাটার একটা এক্সেল ফাইল আছে যা মূলত ব্যাকেন্ডে পাঠাতে হবে ফ্রন্ট এন্ড থেকে সেক্ষেত্রে আপনি যদি কাজ টা মেইন থ্রেডে করতে চান তাহলে অনেক বড় একটা সমস্যা হয়ে যাবে কারণ জাভাসস্ক্রিপ্ট সিঙ্গেল থ্রেডেড ল্যাংগুয়েজ ও সাধারনত ব্লকিং বৈশিষ্ট্য এর এবং এ কারণে যখন সে কোড রান করবে সে কোড এক্সিকিউশন শেষ না হওয়া পর্যন্ত ব্লক হয়ে থাকবে তার মানে আর অন্য কোণ কোড রান করানো যাবে না। এমন প্রব্লেম সল্ভ করতে পারে একমাত্র Woker API. এই API যখন আপনি ব্যাবহার করবেন তখন সে মূলত মেইন থ্রেড কে ব্লক না করে আলাদা একটা থ্রেডে আপনার সে বড় কোডটাকে রান করিয়ে এক্সিকিউশন শেষে রেজাল্ট দিয়ে দেয়।&#x20;

চলুন কিছু উদাহরন দেখিঃ-

{% code lineNumbers="true" %}
```javascript
// worker.js (Worker Script)
function doSomeWork(data) {
  // Simulate some long-running task
  for (let i = 0; i < 100000000; i++) {}
  postMessage({ result: 'Work Done!', data });
}

self.addEventListener('message', (event) => {
  const { data } = event;
  doSomeWork(data);
});

// main.js (Main Script)
const worker = new Worker('worker.js');

worker.postMessage({ someData: 'This is sent to the worker' });

worker.addEventListener('message', (event) => {
  const { data } = event;
  console.log('Worker message:', data);
});

```
{% endcode %}
