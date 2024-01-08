# হিস্ট্রি এপি আই (History API)

**History API** হলো একটি জাভাস্ক্রিপ্ট API যা ব্যাবহার করে   ওয়েব ব্রাউজারের ওয়েব পেইজ **History**  ব্যবহার করা যেতে পারে। এটি ব্যবহার করে বর্তমান পেইজ, পূর্বের পেইজ, এবং পূর্ববর্তী সকলপেইজ সমূহ অ্যাক্সেস করা যায়।&#x20;

**History API** এর কয়েকটি সাধারণ ব্যবহার:

```javascript
// ইতিহাসে পৃষ্ঠার সংখ্যা রিটার্ন করে।
window.history.length

// সাম্প্রতিক পৃষ্ঠাগুলি অ্যাক্সেস করা
const pages = window.history.pages;

// পূর্ববর্তী পৃষ্ঠাটির URL রিটার্ন করা
const previousUrl = window.history.previousUrl;

// বর্তমান পৃষ্ঠার URL রিটার্ন করে।
const currentUrl = window.history.currentUrl 

//n সংখ্যার পৃষ্ঠা পিছনে বা সামনে যায়।
window.history.go(2): 

// বর্তমান পৃষ্ঠা ফিরে যাওয়া
window.history.back();

// বর্তমান পৃষ্ঠা এগিয়ে যাওয়া
window.history.forward();

// একটি নতুন পৃষ্ঠা যুক্ত করা
window.history.pushState({
  title: "নতুন পৃষ্ঠা",
}, "নতুন পৃষ্ঠা", "/new-page");

// একটি পৃষ্ঠাকে প্রতিস্থাপন করা
window.history.replaceState({
  title: "প্রতিস্থাপিত পৃষ্ঠা",
}, "প্রতিস্থাপিত পৃষ্ঠা", "/replaced-page");
```
