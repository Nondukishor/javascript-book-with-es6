# আন্ডিফাইন্ড (Undefined)

**আন্ডিফাইন্ডঃ-** আন্ডিফাইন্ড মানে হলো অনির্দিষ্ট । তার মানে কম্পিউটার এর ভ্যালু জানে না । তাই যখন বুঝতে পারছিলনা এর ভ্যালু কি হবে তখন কম্পিউটার ভাইয়া বলে দেয় আমি ভাই জানি না এর ভ্যালু কি হবে। তাই বলে দেয় অনির্দিষ্ট মানে এর ভ্যালু যে কোন কিছু হতে পারত । হতে পারত সেটা স্ট্রিং , হতে পারত সেটা নাম্বার , হতে পারত সেটা কোন বুলিয়ান কিন্তু কম্পিউটার ভাইয়া জানে কি হবে আর এটায় হলো আন্ডিফাইন্ড।

```javascript
var a;
console.log(a)
```

output:

```javascript
undefied
```

এখানে একটু লক্ষ্য করলে দেখতে পাবেন এখানে a এর জন্য কোন ভ্যালু অ্যাসাইন করা হয়নি তাই কম্পিটার ভাইয়া বুঝতে না পেরে বলে দিয়েছে ভাই আমি তো কিছু জানি না এটা যেকোনো কিছু হতে পারত তাই এর ভ্যালু অনির্দিষ্ট হবে।

**আন্ডিফাইন্ড কখন কখন হবে ?**

১। যদি ফাংশনের কোন রির্টান না থাকে ।

```javascript
function doSomething() {
  // No return statement
}

const result = doSomething();
console.log(result); // Output: undefined
```

২। যদি variable লিখে তাতে কোণ ভ্যালু assign করা না হয়&#x20;

```javascript
let myVariable;
console.log(myVariable); // Output: undefined
```

৩। যদি কোন অব্জেক্টের এমন কী কে এক্সেস করতে চাওয়া হয়

```javascript
const person = {
  name: "John",
  age: 30,
};

console.log(person.gender); // Output: undefined

```

৪। যদি কোণ ফাংশনের প্যারামিটার পাস করা না হয়।

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet(); // Output: Hello, undefined!

```

৫। ভ্যালু assign করে যদি কোন ভাবে পরিবর্তন করা হয়&#x20;

```javascript
let variable = 42;
variable = undefined;
console.log(variable); // Output: undefined

```
