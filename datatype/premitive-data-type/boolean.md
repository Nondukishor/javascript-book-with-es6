# বুলিয়ান (Boolean)

**বুলিয়ানঃ** বুলিয়ান হচ্ছে একটি প্রিমিটিভ বা সনাতন ডাটা টাইপ। এটি শধু মাত্র সত্য কিংবা মিথ্যা বুঝে এর বাইরে কিছু বুঝে না তার মানে হচ্ছে 1 ,0 এর বাইরে কিছুই না কোন ডাটার সত্য মিথ্যা যাচাই করা ক্ষেত্রে এর ব্যবহার লক্ষ্য করা যায় ।

আসুন একটা প্রোগ্রাম করে তার প্রমাণ করে নেই

```javascript
const isActive = true;
if(isActive === true) console.log("Yes sir! I am active in programming");
else console.log('Sorry! I am not active in programming I can not make it');
```

এখানে হয়েছে কি আমরা <mark style="color:red;">isActive</mark> নামে একটি ভেরিএবলে true অ্যাসাইন করেছি । আর পড়ে চেক করেছি <mark style="color:green;">true</mark> কিনা ? যদি true হয় তাহলে কনসোলে <mark style="color:green;">`Yes sir! I am active in programming`</mark> লেখা টা প্রিন্ট করেছি আর যদি <mark style="color:red;">false</mark> মানে মিথ্যা হয় তাহলে আমি <mark style="color:green;">`Sorry! I am not active in programming I can not make it`</mark> এই লেখাটা দেখাতে বলেছি । তার মানে এখন প্রোগ্রাম টার আউটপুট কি হবে আউটপুট হবে <mark style="color:green;">`Yes`</mark> <mark style="color:green;">`sir! I am active in programming`</mark> । আপনি যদি সফল ভাবে আপনার কোডটি লিখে থাকেন তাইলে আপনার কাজ হলো আবার পরের প্রোগ্রামটা করে ফেলা ।

```javascript
const num1=1;
const num2=2;
console.log(num1===num2)
```

output :

```javascript
false
```

এটা যদি করে বুঝে থাকেন তাইলে আপনার কাজ হলো আরে একটি প্রোগ্রাম করে ফেলেন

```javascript
console.log(true === false)
```

output: false

```javascript
console.log(false === true)
```

output:

```javascript
false
```

```javascript
console.log(true === true)
```

output:

```javascript
true
```

#### Boolean Object:&#x20;

ভ্যালু ছাড়া সব কিছু Boolean এ false হিসবে কাউন্ট করে । আবার `0,"",-0,`**`NaN,undefined,null`**কে Boolean false হিসেবে ধরে নেই । চলুন নিচে এগুলোর উদাহরণ দেখে নেই।&#x20;

```javascript
let zoro = 0;
let one = 1;
let emptyString = "";
let nullvalue = null;
let undefinedValue = undefined;
let NaNvalue = NaN;

console.log(Boolean(zero)) // false
console.log(Boolean(one)) // false
console.log(Boolean(emptyString)) // false
console.log(Boolean(nullvalue)) // false
console.log(Boolean(undefinedValue)) // false
console.log(Boolean(NaNvalue)) // false
```

