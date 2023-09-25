# এন এফ ই (NFE)

NFE(Name Function Entity) বুঝার আগে চলুন একটু পিছনে যায়। আমারা জানি জাভাস্ক্রিপ্ট অবজেক্ট বলে একটা ডাটা টাইপ আছে। জাভাস্ক্রিপ্টে ফাংশন অবজেক্ট হিসবে কাজ করে । ফাংশন জাভাস্ক্রিপ্টে অনেকগুলো সুবিধা দিয়ে থাকে যেমন ফাংশনকে কল করা যায়। অবজেক্ট এর মতো করে ডাটা যুক্ত করা যায় এবং বাদ দেওয়া যায়।&#x20;

আরো গভীরে যাওয়ার আগে আমরা একটা উদাহরণ দেখে নিই চলুনঃ-

```javascript
function ask(question, ...handlers) {
  let isYes = confirm(question);

  for(let handler of handlers) {
    if (handler.length == 0) {
      if (isYes) handler();
    } else {
      handler(isYes);
    }
  }

}

// for positive answer, both handlers are called
// for negative answer, only the second one
ask("Question?", () => alert('You said yes'), result => alert(result));
```
