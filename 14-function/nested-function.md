# ক্রিয়াকলাপের ভিতরে ক্রিয়াকলাপ ( Nested Function)

ক্রিয়াকলাপের ভিতরে ক্রিয়াকলাপ বা নেস্টেড ফাংশন কে অনেক সময় সাব রুন্টিন ও বলা হয়। যখন একটা ফাংশন এর ভিতরে আরেকটা ফাংশন কে লিখা হয় তখন আমারা সেইটা কে নেস্টেট ফাংশন বলব। মূলত এই ধরনের ফাংশন গুলো আপনার অভ্যন্তরীন ফাংশনালিটি নিয়ে কাজ করে। যখন আপনার মনে হবে কোন কাজকে ঐ ফাংশনের ভিতরে অনেকগুলো ক্ষুদ্র ক্ষুদ্র ভাগে বিভক্ত করে করা উচিত তখন আসলে নেস্টেড ফাংশন লিখা হয়। বিষয় টা কে আপনি আপানার ম্যাথ এর সাথে মিলাতে পারেন $$(x,n,a)=f(x,n,4)=\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}}}}}$$ এই ধরনের কনসেপ্ট গুলো চিন্তা করলেই বুঝতে পারবেন আসলে নেস্টেট ফাংশন কিভাবে আসলে কেন লিখা হয়

$$(x,n,a)=f(x,n,4)=\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}}}}}$$ এর নেস্টেট ফাংশন ব্যাবহার করে সামধান&#x20;

```javascript
function solveEquation(x, n, a) {
  function nestedExpression(currentX, currentN) {
    if (currentN === 1) {
      return Math.pow(currentX, n - 1); // Base case: n = 1
    } else {
      return Math.pow(currentX, n - 1) * nestedExpression(currentX, currentN - 1);
    }
  }

  function recursiveRoot(currentX, currentN) {
    if (currentN === 1) {
      return Math.pow(currentX, 1 / n); // Base case: n = 1
    } else {
      return Math.pow(nestedExpression(currentX, currentN), 1 / n) * recursiveRoot(currentX, currentN - 1);
    }
  }

  return recursiveRoot(x, a);
}

const x = 2; // Replace with the value of x you want to use
const n = 3; // Replace with the value of n you want to use
const a = 4; // Replace with the value of a you want to use

const result = solveEquation(x, n, a);
console.log(`Result: ${result}`);

```

আরো কিছু যদি উদাহরন দেখিঃ

* $$\sqrt{1+2\sqrt{1+3\sqrt{}1+4}}$$

```javascript
function solveEquation() {
  function nestedExpression(n) {
    if (n === 1) {
      return Math.sqrt(1 + 4); // Base case: n = 1
    } else {
      return Math.sqrt(n + (n - 1) * nestedExpression(n - 1));
    }
  }

  return nestedExpression(4);
}

const result = solveEquation();
console.log(`Result: ${result}`);

```

* $$x = \sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}\sqrt[n]{x^{n-1}}}}$$

```javascript
function solveEquation(x, n, iterations) {
  function nestedExpression(currentX, remainingIterations) {
    if (remainingIterations === 0) {
      return currentX;
    } else {
      const innerExpression = Math.pow(currentX, n - 1);
      return nestedExpression(Math.pow(innerExpression, 1/n), remainingIterations - 1);
    }
  }

  return nestedExpression(x, iterations);
}

const x = 2;
const n = 3;
const iterations = 5;

const result = solveEquation(x, n, iterations);
console.log(`x = ${result}`);

```

