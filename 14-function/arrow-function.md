# তীর ক্রিয়াকলাপ(Arrow Function)

অ্যারো ফাংশনটা মূলত ES6 সংযোজন। মূলত রেগুলার ফানশনের কিছু লিমিটেশন কে কেন্দ্র করেই  অ্যারো ফাংশন বানানো হয়েছে। অ্যারো ফাংশন হচ্ছে নাম বিহীন ফাংশন লিখার সংক্ষিপ্ত রুপ অ্যারো ফাংশনের সাথে রেগুলার ফাংশনের যে বড় তফাত সেইটা হলো ত  <mark style="color:red;">**`this`**</mark> keyword এর  রেগুলার ফাংশনে this ঐ ফাংশন স্কোপ কে বুঝায় আর অ্যারো ফাংশনে সেইটা window object কে বুঝায়।&#x20;

অ্যারো ফাংশনের সিনট্যাক্সঃ&#x20;

```javascript
const functionName = (parameters) => {
  // function body
  return value;
};

```

উদাহরনঃ&#x20;

```javascript
const add=(num1, num2)=> {
  const sum = num1 * num2
  return sum
}
```

অ্যারো ফাংশন বৈশিষ্ট্যঃ

* যদি আর্গুমেন্ট না থাকে এবং একটি মাত্র স্টেটমেন্ট থাকে।

```javascript
const multiply = () => 2 * 2;
multiply(2) // output 4
```

* যদি আর্গুমেন্ট থাকে এবং একটি মাত্র স্টেটমেন্ট থাকে।

```javascript
const multiply = a => a * 2;
multiply(2) // output 4
```

* কলব্যাক ফাংশন হিসেবে।

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8, 10]

const even = numbers.filter(num => num % 2 === 0);
console.log(even); // Output: [2, 4]
```

* রেগুলার আর অ্যারো ফাংশনের মাঝে পার্থক্য।&#x20;

```javascript
const person = {
  firstName: "Nipu",
  lastName: "Chakraborty",
  fullName: function() {
    // Using traditional function to access object properties
    return this.firstName + " " + this.lastName;
  },
  arrowFullName: () => {
    // Arrow function does not have its own 'this'
    // It uses the 'this' value of the surrounding code
    return this.firstName + " " + this.lastName;
  }
};

console.log(person.fullName());     // Output: Nipu Chakraborty
console.log(person.arrowFullName()); // Output: undefined undefined

```

এইখানে দেখতেই পাচ্ছেন রেগুলার ফাংশনের this কিন্তু ঐ অবজেক্ট এর স্কোপকেই বুঝাচ্ছে। আর অ্যারো ফাংশন কিন্তু ঐ অবজেক্ট স্কোপ কে বুঝাচ্ছে না।&#x20;

তাছাড়া রেগুলার ফাংশন কে কিন্তু কন্সট্রাক্টর ফাংশন হিসবেও ব্যবহার করা যায় কিন্তু অ্যারো ফাংশন কে কন্সট্রাক্টর ফাংশন হিসেবে ব্যবহার করা যায় না।&#x20;
