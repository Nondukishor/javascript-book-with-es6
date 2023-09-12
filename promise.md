# প্রমিস (Promise)

প্রমিস বিষয়টার অর্থ হলো **প্রতিশ্রুতি** মানুষের দৈনন্দিন জীবনের সাথে প্রমিস একদম উতপ্রেত ভাবে জড়িত। ধরে নিন আপনি কাউকে কথা দিলেন যে আগামীকাল আপনি তার বাড়িতে বেড়াতে যাবেন এখন যাওয়ার জন্য অনেক সময় লাগতে পারে ধরে নিলাম ২০ মিনিট কিন্তু আপনি যে আসলে ২০মিনিটে পৌছাবেন এইটা আপনি নির্দিষ্ট না কারন রাস্তায় জ্যাম থাকতে পারে গাড়ি নষ্ট হতে পারে বা গাড়িড় তেল মাঝ পথে শেষ হতে পারে অথবা রাস্তা ফাকা থাকার কারনে আপনি ২০ মিনিটের আগেই পৌছাতে পারেন। এইখানে একটা বিষয় লক্ষ্য করুন ভাল করে আপনি কিন্তু কথা দিয়েছেন যাবেন কিন্তু আপনার যে যাওয়া হবে এইটা আপনি সবসময় নিশ্চত না। আপনি যদি কোন কারণে যেতে না পারেন আপনি দুঃখিত হবেন এবং যাকে কথা দিয়েছেন থাকে ফোন করে বা কোন ভাবে হয়ত সরি বলবেন। আর যদি যেতে পারেন তাহলে তো আপনি খাওয়া দাওয়া করে খুশি খুশি অনুভব করবেন। জাভাস্ক্রিপ্টের প্রমিস ও টিক একই রকম। এইখানে প্রমিসে আপনি কিছু একটা দিবেন সে প্রথমে চেষ্টা করবে resolve করতে কিন্তু কো কারনে যদি করতে না পারে তাহলে সে reject করবে মানে আপনাকে সে বলবে আমি আসলে প্রমিস টা রাখতে পারলাম না।&#x20;

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

{% code title="কলব্যাক যেভাবে লিখতাম " lineNumbers="true" %}
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



{% code title="Promise এ যেভাবে লিখতে হবে" lineNumbers="true" %}
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
