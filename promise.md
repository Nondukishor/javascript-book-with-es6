# প্রমিস (Promise)

প্রমিস বিষয়টার অর্থ হলো **প্রতিশ্রুতি** মানুষের দৈনন্দিন জীবনের সাথে প্রমিস একদম উতপ্রেত ভাবে জড়িত। ধরে নিন আপনি কাউকে কথা দিলেন যে আগামীকাল আপনি তার বাড়িতে বেড়াতে যাবেন এখন যাওয়ার জন্য অনেক সময় লাগতে পারে ধরে নিলাম ২০ মিনিট কিন্তু আপনি যে আসলে ২০মিনিটে পৌছাবেন এইটা আপনি নির্দিষ্ট না কারন রাস্তায় জ্যাম থাকতে পারে গাড়ি নষ্ট হতে পারে বা গাড়িড় তেল মাঝ পথে শেষ হতে পারে অথবা রাস্তা ফাকা থাকার কারনে আপনি ২০ মিনিটের আগেই পৌছাতে পারেন। এইখানে একটা বিষয় লক্ষ্য করুন ভাল করে আপনি কিন্তু কথা দিয়েছেন যাবেন কিন্তু আপনার যে যাওয়া হবে এইটা আপনি সবসময় নিশ্চত না। আপনি যদি কোন কারণে যেতে না পারেন আপনি দুঃখিত হবেন এবং যাকে কথা দিয়েছেন থাকে ফোন করে বা কোন ভাবে হয়ত সরি বলবেন। আর যদি যেতে পারেন তাহলে তো আপনি খাওয়া দাওয়া করে খুশি খুশি অনুভব করবেন। জাভাস্ক্রিপ্টের প্রমিস ও টিক একই রকম। এইখানে প্রমিসে আপনি কিছু একটা দিবেন সে প্রথমে চেষ্টা করবে resolve করতে কিন্তু কো কারনে যদি করতে না পারে তাহলে সে reject করবে মানে আপনাকে সে বলবে আমি আসলে প্রমিস টা রাখতে পারলাম না।&#x20;

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption><p>image ref : <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/promises.png">https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/promises.png</a></p></figcaption></figure>

দেখে নেই প্রমিস কিভাবে লিখতে হবে?

```javascript
const meetingTime = "10:00 AM"
const reachTime = "10:30 AM"
const promise = new Promise((resolve, reject)=>{
  if(meetingTime === reachTime){
     resolve("Promise resolved")
  }
  else{
    reject("Promise Rejected")
  }
})
```

#### কেন আমরা প্রমিস লিখব?

প্রমিস লিখার মূল কারন হলো আগে যে আমরা কলব্যাক ফাংশন ব্যাবহার করতাম সেইখানে আমাদের কন্ট্রোল ছিল না তাছাড়া কোড ম্যানেজ করা কষ্টসাধ্য ছিল এরর হ্যান্ডেলিং করা জটিল ছিল এসব সমসার সমাধান করার জন্যই মূলত প্রমিসের উদ্ভব হয়েছে।&#x20;

চলুন দেখে নেই কলব্যাক আর প্রমিসের মাঝে পার্থক্যটা কোথায় ?

কলব্যাক যেভাবে লিখতাম

{% code title="callback.js" lineNumbers="true" %}
```javascript
function fetchData(callback) {
  setTimeout(() => {
    const data = 'Fetched data';
    callback(data);
  }, 1000);
}

fetchData((result) => {
  console.log(result);
});

```
{% endcode %}

Promise এ যেভাবে লিখতে হবে

{% code title="promise.js" lineNumbers="true" %}
```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const data = 'Fetched data';
      resolve(data);
    }, 1000);
  });
}

fetchData()
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.error(error);
  });
```
{% endcode %}

#### প্রমিস লিখে সুবিধা কি কি পাচ্ছি?

১। প্রমিস লিখার মাধ্যমে আমি আমার কোড গুলো ছোট অংশে ভাগ করতে পারছি।

২। প্রমিসের চেইনিং মেথড গুলো ব্যাবহার করে আমি ডাটা ম্যানুপুলেট ও কাষ্টমাইড করতে পারছি।

৩। বিল্ড ইন এরর হ্যান্ডেলিং সিন্ট্যাক্স পাচ্ছি।

৪। এক সাথে অনেক গুলো প্রমিস কে ব্যাচ অপারেশন হিসেবে প্রসেস করতে পারছি।

৫। সহজে Asynchronous অপারেশন হ্যান্ডেল করতে পারছি।



#### Promise.any()

#### Promise.all()

#### Promise.race()

#### Promise.allSettled()

