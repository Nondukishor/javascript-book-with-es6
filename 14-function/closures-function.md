# বন্ধ ক্রিয়াকলাপ(Closures Function)

বন্ধ ক্রিয়াকলাপ(Closures Function) মানে হচ্ছে কোন কিছু কে আবদ্ধ করে রাখা। আরো যদি সহজ ভাষায় বলি কোন কিছু নিজের একটা প্রাইভেট বা ব্যাক্তিগত বক্স করে সেই বক্সে রাখা। সেইটা কেন কেন? আপনার মনে প্রশ্ন আসতে পারে এখন।&#x20;

MDN এর অফিসিয়াল সংজ্ঞাঃ&#x20;

> A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

```javascript
function wrapValue(n) {
  let local = n;
  return () => local;
}

let wrap1 = wrapValue(1);
let wrap2 = wrapValue(2);
console.log(wrap1());
// → 1
console.log(wrap2());
// → 2
```
