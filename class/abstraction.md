# অবস্ট্রাকশন(Abstraction)

**Alfred John Cole** এবং **Ronald Morrison** 1982 সালে এই অবস্ট্রাকশন বিষয় সর্ব প্রথম ধারনা দেন এবং সেইটা **An introduction to programming with S-algol** বইয়ের মাধ্যমে ধারণা দেন হয় পরে Bruce J. MacLennan (1983) Principles of programming languages এর উপর design, evaluation, and implementation নিয়ে বিস্তারিত লিখে আরেকটি বই প্রকাশ করে যার মূল লক্ষ্য ছিল "Avoid requiring something to be stated more than once" অনেকটা এখন আমরা যে বলি **ডু নট রিপিট ইউরসেলফ (DRY)**&#x995;থাটা কে বুজায়। মতামত উপস্থাপন করেন আর পরে এইটার দিনের পরে আরো উন্নতি হয় এবং OOP তে খুব জনপ্রিয়তা পায়।&#x20;

আমার গল্প বলতে ভালই লাগে তাই আবার গল্প দিয়েই শুরু করি। আপনার কাছে যে কম্পিউটারটা আছে সেইটা অনেক যন্ত্রপাতি দিয়ে তৈরী আপনি শুধু মাত্র ব্যাবহার করছেন। এখানে অনেক রকমের ইলিমেন্ট আছে এবং সেগুলো একেকটার কাজ কিন্তু একেক রকম । এখন যদি প্রশ্ন করি প্রসেসর কিভাবে তৈরী আপনি হিমশীম খেয়ে যাবেন কারন আপনি জানেন ই না বা হয়ত। এই যে লুকোচুরি ব্যাপার টা সেইটায় হলো অবস্ট্রাকশন(Abstraction)। আপনি যখন আপনার কম্পিউটারটা ব্যবহার করছেন শুধু মাত্র একটা বাটন টিপ দিচ্ছেন আর সাথে সাথে আপনার কম্পিউটারটা অন হয়ে যাচ্ছে ।

আরো যদি বলি আপনার একটা মোবাইল আছে সেইটাতে বিভিন্ন ফাংশনালিটি আছে সেগুলো কিভাবে কাজ করেছে কেমন করে করছে তা আপনি জানেন না কিন্ত আপনি সেসব ফাংশনালিটি ব্যাবহার করে হয়ত সুবিধা নিচ্ছেন এইটাই মূলত অবস্ট্রাকশন।&#x20;

এরকম আরও যদি চিন্তা করতে চান আপনি মাইক্রো ওভেন ও কার এগুলো নিয়েও চিন্তা করতে পারেন।

এবার চলুন পোগ্রামিং করে বিষয় টা আরেকটু বুঝি উদাহরণ এর মাধ্যমেঃ-

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

const person = new Person('Alice', 30);
person.greet();
```

অবস্ট্রাকশন অনেকভাবেই হতে পারে তবে দুই ধরণের ক্যাটাগরি তে একে ফেলা যায় সেগুলো হচ্ছেঃ-

1. **ডাটা অবস্ট্রাকশন**
2. **প্রসেস অবস্ট্রাকশন**

**ডাটা অবস্ট্রাকশনঃ-** আবার গল্পে গল্পে বুঝে নেই আসলে ডাটা অবস্ট্রাকশন কি?&#x20;

ধরে নিলাম আপনার একটা ব্যাংক একাউন্ট আছে ব্যাংকের নাম হচ্ছে **মধুমালতী** ব্যাংক। এখন আপনি সেখানে টাকা রাখেন। রাখার আপনার টাকার পর এখানে অনেক অনেক জটিল হিসাব নিকাশ হয়। এছাড়া আপনি যখন  **মধুমালতী** ব্যাংক থেকে টাকা উত্তোলন করেন তখন ও কিন্তু অনেক ডাটা রিলেটেড হিসাব নিকাশ হয়। এই যে এত্ত ডাটার হিসাব নিকাশ হলো সেইটা কিন্তু আপনি একদম ই জানেন না কিভাবে হচ্ছে? কোন ডাটার সাথে হচ্ছে হয়ত আপনি একটা Higher Level এর ধারণা পাচ্ছেন এতে কোনো আপত্তি নেই কিন্তু ডাটাবেজের কোন কলাম কোন টেবিল বা কোন লজিকে ডাটা গুলো ক্যাল কুলেশন হচ্ছে একদম ই চোখে দেখছেন না হয়ত। আরো বুঝার জন্য চলুন আরো কিছু উদাহরন নিয়ে আলোচনা করি। তারপর আমরা আসলে রিয়েল টাইম কিছু উদাহরন দেখব। যেগুলো আমরা ভবিষ্যৎ এ কাজে লাগাব।&#x20;

{% code title="Data hiding example" overflow="wrap" lineNumbers="true" %}
```javascript
class BankAccount {
  constructor(accountNumber, balance = 0) {
    this.accountNumber = accountNumber; // Private data
    this.balance = balance; // Private data
  }

  // Method to get the account balance (data access)
  getBalance() {
    return this.balance;
  }

  // Method to deposit money (data modification)
  deposit(amount) {
    if (amount > 0) {
      this.balance += amount;
      console.log(`Deposited $${amount}. New balance: $${this.balance}`);
    } else {
      console.log('Invalid deposit amount.');
    }
  }

  // Method to withdraw money (data modification)
  withdraw(amount) {
    if (amount > 0 && amount <= this.balance) {
      this.balance -= amount;
      console.log(`Withdrawn $${amount}. New balance: $${this.balance}`);
    } else {
      console.log('Invalid withdrawal amount or insufficient balance.');
    }
  }
}

const myAccount = new BankAccount('12345');
console.log(`Account ${myAccount.accountNumber} balance: $${myAccount.getBalance()}`);
myAccount.deposit(100);
myAccount.withdraw(50);

```
{% endcode %}

ধরুন আপনি একটা অ্যাপ্লিকেশন বানাচ্ছেন সেখানে ইউজার রেজিস্ট্রেশন করতে পারে লগিন করতে পারে  আর ইউজার এর ডাটা নিতে পারে। এখন এই অ্যাপ্লিকেশন আপনি নিশ্চয় ইউজারের ডাটা নেওয়ার সময় সব ডাটা নিবেন না যেমন পাসওয়ার্ড বা তার পিন কোড। এই যে আপনি ডাটা টা নিলেন না মানে আপনার কাছে ডাটা নাই তা কিন্তু না আপনি শুধু মাত্রা ডাটা টা লুকিয়ে রাখছেন একই বিষয় টা হতে পারে ATM কার্ড এর ক্ষেত্রে পিন নাম্বার হ্যাশ করে রাখা। একই বিষয় টা হতে পারে আপনার কোন সিক্রেট টোকেন হাইড করে রাখা।&#x20;

**প্রসেস অবস্ট্রাকশন:** প্রসেস অবস্ট্রাকশন বিষয় টা কিন্তু একই রকম ডাটা **অবস্ট্রাকশন** এর মতই কিন্তু বিষয় শুধু ডাটা এর জায়গায় প্রসেস গুলো কে লুকায়িত করা হচ্ছে।&#x20;

আবার একটা গল্পে গল্পেই বলি। ধরুন আপনার একটা ওয়াসিং মেশিন আছে এবং সে ওয়াসিং মেশিনের নাম হচ্ছে WWWC(Without wife Wash Cloth) এখন এই মেশি WWWC মেশিন টা তে আপনি যদি প্রয়োজন মতো ওয়াশিং পাঊডার আর কাপড় দিয়ে দেয় তাহলেই সে আপনাকে ঝকঝকে চক চকে কাপড় দিয়ে দিবে কিন্ত এই যে WWWC আপনার কাপড় টা ধুয়ে দিল কেমন করে করল? কিভাবে করল? কোন প্রসেস এ করল সেইটা আপনার একদম লুকানো । সুতরাং এই যে পদ্ধতি এইটা পুরোটায় হলো প্রসেস হাইডিং।&#x20;

চলুন উদাহরণ দেখি একটাঃ-

{% code title="Process hiding example" overflow="wrap" lineNumbers="true" %}
```javascript
class WashingMachine {
  constructor() {
    this.powerOn = false; // Private data
    this.waterLevel = 0;  // Private data
    this.currentCycle = ''; // Private data
  }

  // Method to turn on the washing machine (data modification)
  turnOn() {
    if (!this.powerOn) {
      this.powerOn = true;
      console.log('Washing machine is now on.');
    } else {
      console.log('Washing machine is already on.');
    }
  }

  // Method to select a washing cycle (data modification)
  selectCycle(cycle) {
    if (this.powerOn) {
      this.currentCycle = cycle;
      console.log(`Selected ${cycle} cycle.`);
    } else {
      console.log('Please turn on the washing machine first.');
    }
  }

  // Method to set the water level (data modification)
  setWaterLevel(level) {
    if (this.powerOn) {
      this.waterLevel = level;
      console.log(`Water level set to ${level}.`);
    } else {
      console.log('Please turn on the washing machine first.');
    }
  }

  // Method to start the washing cycle (hidden process)
  startWash() {
    if (this.powerOn && this.currentCycle !== '' && this.waterLevel > 0) {
      console.log(`Starting the ${this.currentCycle} cycle with water level ${this.waterLevel}.`);
      // Simulate washing

```
{% endcode %}

