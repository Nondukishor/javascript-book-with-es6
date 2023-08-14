---
description: >-
  সতর্ক বার্তাঃ কেউ যদি বইটির কোন অংশ খারাপ উদ্দেশ্যে বা বাণিজ্যিক উদ্দেশ্য
  ব্যভার করে তাহলে কপিরাইট আইন অন্তর্ভুক্ত সকল প্রকার প্রক্রিয়া অনুসরণ করতে
  বাধ্য থাকব।
---

# ⚒ কন্ডিশনাল কন্ট্রোল ফ্লো(Conditional Control flow)

একজন প্রোগ্রামারের যদি কন্ডিশনাল বা শর্ত যুক্ত লজিক চালাইতে হয় সে ক্ষেত্রে যে টপিকটা বেশি বেশি করে জানা প্রয়োজন সেটা হচ্ছে কন্ডিশনাল কন্ট্রোল ফ্লো স্টেটমেন্ট । তো চলুন কিভাবে এটা কাজ করে

কন্ডিশনাল কন্ট্রোল ফ্লো হচ্ছে শর্তের উপরে নির্ভরশীল যেরকম শর্ত আরোপ করবেন সেইরকম কাজ করবে।

কন্ডিশনাল কন্ট্রোল ফ্লো বলতে চারটা টপিকে সাধারণত বুঝায় আর সেটা হলো।

**১। শুধু if statement**

**২। if এবং else statement**

**৩। if ,else if এবং else statement**

**৪। switch statement**

তো আমি চেষ্টা করব এই বইটির মাধ্যমে আমি যতটুকু জানি তা যথাসাধ্য তুলে ধরার । তো আসুন শুরু করা যাক প্রথমে if statement দিয়ে

**১। শুধু if statement**

সিন্ট্যাক্সঃ

```javascript
if(conditon){
  ---your statement---
}
```

এইটাই হচ্ছে শুধু if দিয়ে কন্ডিশন চালানোর সিনট্যাক্স।

এবার দেখি চলেন একটা উদাহরন

```javascript
if(true){
    console.log("Hello! It's true");
}
```

এখানে আমি যেটা বললাম সেটা হলো যদি সত্য হয় তাহলে কন্সোলে ''Hello! It's true" লেখাটা দেখাও । আপনি প্রোগ্রামটা লিখে রান করে দেখেন আসলে টিক টাক মতো কাজ করছে কিনা আর যদি করে থাকে তাহলে তো ভাল আর না করলে মেইল করে দেন আমাকে আমি একটু করে চেষ্টা করে দেখব আশা করি আপনার সেটা দরকার হবে না।

এবার দেখি আরেকটা প্রোগ্রাম লিখে ফেলি।

```javascript
let name='Nipu Chakraborty'

if(name==='Nipu Chakraborty'){
    console.log('Welcome! your name is'+name)
}
```

ব্যাখ্যাঃ এখানে আমি যা করেছি সেটা হলো একটা variable নিয়েছি 'name' নামে আর ওখানে আমি ভেলু অ্যাসাইন করেছি আমার নামটা মানে 'Nipu Chakraborty' । এর পর আমি চেক করেছি 'name' নামে যে ভ্যারিএবল টা আছে সেটাতে আসলে কি আমার নাম আছে কিনা মানে "Nipu Chakraborty" আছে কিনা আর যদি থাকে তাহলে আমি বলেছি আমাকে যেন সে কনসোলে 'Welcome! your name is Nipu Chakraborty' লেখাটা দেখায়। যেহেতু আছে সেহেতু আমার এই প্রোগ্রামটার আউটপুট হবে।

```javascript
Welcome! your name is Nipu Chakraborty
```

তো এখন আমরা দেখব কিভাবে if এবং else দিয়ে কন্ডিশন চালানো যায়।

**২। if এবং else statement**

সিনট্যাক্সঃ-

```javascript
if(condition){
  //statement
}else{
  //statement
}
```

if এবং else যুক্ত কন্ডিশনের ক্ষেত্রে প্রথমে ধাপে শর্ত সত্য হলে যে statement run হবে সেটা লিখতে হয়। আর ২য় ধাপে শর্ত সত্যি না হলে কি হবে সেটা লিখতে হয় ।

তো চলুন একটা উদাহরন দেখে নেই

```javascript
let isActive = true;

if(isActive===true){
  console.log("It's true you are active");
}
else{
  console.log("Sorry you are not active")
}
```

ব্যাখ্যাঃ- এখানে যা ঘটেছে তা হলো প্রথমে আমি একটা varible নিয়েছি isActive নামে তার পর আমি প্রথম ধাপে বলেছি isActive varible এ true আছে কিনা ? আর যদি থাকে তাহলে কনসোলে যেন `It's true you are active` লেখাটা দেখায়। আর যদি isActive সমান true না হয় তাহলে যেন কনসোলে `Sorry you are not active` লেখাটা দেখায়

যেহেতু এখানে isActive সমান true সেহেতু এখানে প্রোগ্রামটার আউটপুট হবে `It's true you are active`

এখন আপনার কাজ হলোঃ-

প্রোগ্রামটা হুবুহু লিখে isActive এর value কে false করে দেওয়া এর কি আউটপুট আসে তা দেখা আর সেটা কেন এসেছে তা আমাকে জানানো।

এবার আমরা দেখব if , if else এবং else কিভাবে কাজ করে এবং এদের সিনট্যাক্স কেমন ।

**৩। if ,else if এবং else statement**

সিনট্যাক্স:-

```javascript
if(condition){
   //statement 1
}
else if(condition2){
  //statement 2
}
....
...
else{
 //statement n
}
```

if , if else এবং else এর ক্ষেত্রে যদি প্রথম if কন্ডিশনটা সত্য না হয় তাহলে পরবর্তী if else এর শর্ত কাজ করে এরপর ২য় টি কাজ না করলে তারপরবর্তী if else শর্ত কাজ করে আর এভাবে চলতে থাকে আর শেষ পর্যন্ত এভাবে কোনটা যদি কাজ না করে তাহলে else কাজ করে।

```javascript
var mark = 80;
if(mark=== 80){
    console.log('A+')
}
else if(mark=== 70){
    console.log('A')   
 }
else if(mark=== 60){
    console.log('B')
}
else if(mark=== 50){
    console.log('C')
}
else if(mark===40){
  	console.log('D')      
}
else{
    console.log('F')
}

```

আশা করি আপনি বুঝে গেছেন কি ঘটেছে এইখানে।

ব্যাখ্যাঃ- এখানে যেটা ঘটেছে সেটা হচ্ছে 'mark' নামে একটি ভেরিয়্যাবল নেওয়া হয়েছে এবং প্রথম ধাপে চেক করা হয়েছে আসলে কি mark এর জন্য মান 80 কিনা যদি তাই হয় তাহলে কনসোলে দেখাতে বলেছি 'A+'। টিকে একি ভাবে পরবর্তী ধাপে 70 হলে 'A' এভাবে পরবর্তী ধাপ গুলো দেখাতে বলেছি কিন্তু একদম শেষে আমি যা করেছি সেটা হলো এখানে যা বলেছি মানে তা যদি সত্য না হয় তাহলে যেন else এর মধ্যে যা আছে তাই দেখায় । মানে 'F' দেখায়।

**৪। **<mark style="color:red;">**switch**</mark>** statement**

<mark style="color:red;">**switch**</mark> statement আসলে অনেকটা if else এর মত কাছ করে তবে পার্থক্য হলো এটা কোন একটা মানের উপর নির্ভর করে case বাচাই করে এবং যে কেইসের সাথে মিলে যা সেই case এর কোড গুলোর নির্দেশনা অনুযায়ী কাজ করে।আপনি  <mark style="color:red;">**switch**</mark> statement কে অনেকটা আমাদের লাইটের সুইচ এর মতো করে চিন্তা করতে পারেন পার্থক্য শুধু একটাই। লাইটের সুইচে দুইটা অপশন থাকে কিন্তু প্রগ্রামিং সুইচে আপনি অনেক অপশন যুক্ত করতে পারবেন।&#x20;

**সিনট্যাক্স:-**

```javascript
switch (expression) {
  case value1:
  	//statement for value 1
  	//what should result for statement 1
    break;
  case value2:
     	//statement for value 2
  	//what should result for statement 2
    break;
  case valueN:
  	//statement for value N
  	//what should result for statement N
    break;
  default:
 	//if not match any case then show default statement
    break;
}
```

Example:hammer:

<pre class="language-javascript"><code class="lang-javascript"><strong>let age=10;
</strong>switch(age){
    case age>=10:
        console.log("Your age is less then 10 or 10");
        break;
    case age>=18:
        console.log("Your age is less then 18 or 18");
        break;
    case age>=30:
        console.log("your are is less then 30 or 30");
        break;
    default:
        console.log("Your age is not define please define your age")
        break;
}
</code></pre>

উপরের উদাহরনে দেখা যাচ্ছে আমি প্রথমে এইখানে একটা variable নিয়েছি তারপর সেই  variable এর উপর ভিত্তি করে বিভিন্ন case নিয়েছি সবশেষে একটা default case নিয়েছি আর প্রথমেই লক্ষ্য করলেই দেখতে পাবেন switch একটা প্যারামিটার নেয়। আর সেই প্যারামিটারের উপর ভিত্তি করে case এক্সিকিউট হয় আর যদি কোনটাই না মিলে তাহলে default case ব্লক এক্সিকিউট হয়।&#x20;

আপনি চাইলে নেস্টেট সুইচ কেস লিখতে পারেন নিচে একটা উদাহরন দেখানো হলো।&#x20;



```javascript
let lucky_man = {
      name: "Nipu Chakraborty",
      serial_no: "777777000077777"
      price: 10000
  },
 
switch(lucky_man){
    case lucky_man.name.startsWith('N') === true:
        swich(lucky_man.serial_no){
           case "777777000077777":
                console.log("First lucky man")
            break;
        }
        break;
    case age>=18:
        console.log("Your age is less then 18 or 18");
        break;
    case age>=30:
        console.log("your are is less then 30 or 30");
        break;
    default:
        console.log("Your age is not define please define your age")
        break;
}
```
