# আই. আই. এফ. ই. (IIFE)

**IIFE** এর পুরো নাম হলো **(Immediately Invoked Function Expression)**। এই এর আসলে নাম হওয়া উচিত ছিল আমার মাঝে মাঝে মনে হয় **anonymous self-invoking function** কারন এইটা আসলে একটা নাম ছাড়া ফাংশন কে কল করে যা আপনার কল করা লাগবে না মানে হলো সে নিজেই নিজেকে কল করে আরকি।&#x20;

লিখার নিয়মঃ

{% hint style="info" %}
১। ( প্রথম বন্ধনি দিয়ে শুরু হবে এবং শেষ হবে।

২। একটা নাম বিহীন ফাংশন দিয়ে শুরুন বন্ধনি এর ভিতরে

৩। বিবৃতি গুলো ফাংশনের ভিতরে লিখতে হবে।

৪। শেষে () দিয়ে শেষ করতে হবে
{% endhint %}

উদাহরণঃ&#x20;

```javascript
(function () {
    console.log("Hello I am IIFE");
})()
```

**কখন আপনি অবিলম্বে আমন্ত্রিত ক্রিয়াকলাপ অভিব্যক্তি ব্যাবহার করবেন (IIFE)?**

১। আপনি যখন চাইবেন আপনার কিছু কোড গ্লোবাল স্কোপ থেকে আলাদা করতে।

{% code overflow="wrap" lineNumbers="true" %}
```javascript
const counterModule = (function() {
  let count = 0;

  function increment() {
    count++;
  }

  function decrement() {
    count--;
  }

  function getCount() {
    return count;
  }

  return {
    increment,
    decrement,
    getCount
  };
})();

console.log(counterModule.getCount()); // Output: 0
counterModule.increment();
console.log(counterModule.getCount()); // Output: 1
counterModule.decrement();
console.log(counterModule.getCount()); // Output: 0

```
{% endcode %}

২। মডিউল প্যাটার্ন নামে একটা বিষয় আছে সেইটা যখন লিখতে যাবেন।

{% code overflow="wrap" lineNumbers="true" %}
```javascript
const myModule = (function() {
  // Private variable
  let privateData = "I am private";

  // Private function
  function privateFunction() {
    console.log("This is a private function");
  }

  // Public members
  return {
    // Public method that accesses private data
    getPrivateData: function() {
      return privateData;
    },

    // Public method that calls private function
    publicMethod: function() {
      console.log("This is a public method");
      privateFunction();
    }
  };
})();

console.log(myModule.getPrivateData()); // Output: I am private
myModule.publicMethod(); // Output: This is a public method / This is a private function

```
{% endcode %}

৩। প্রাইভেট Asynchronous Operations অপারেশন এর ক্ষেত্রে।

{% code overflow="wrap" lineNumbers="true" %}
```javascript
(function() {
  // Your IIFE encapsulated code
  const data = 'Initial data';

  (async function() {
    try {
      const fetchedData = await fetchData();
      console.log(fetchedData); // Output: Fetched data
    } catch (error) {
      console.error(error);
    }
  })();

  async function fetchData() {
    return new Promise(resolve => {
      setTimeout(() => {
        const data = 'Fetched data';
        resolve(data);
      }, 1000);
    });
  }
})();

```
{% endcode %}
