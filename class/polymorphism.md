# পলিমরফিজম (Polymorphism)

পলিমরফিজম (Polymorphism) বা বহুরূপতা একটি গ্রিক্ শব্দ যার অর্থ একাধিক আকার গ্রহণ করার ক্ষমতা। ধরে নিন আপনার নাম জিরো আলম।এখন আপনার পরিচয় আপনার বন্ধুদের কাছে বন্ধু , আপনার বাবার কাছে ছেলে আবার আপনার প্রিয়তমার কাছে বাবু/ প্রিয়তম/ জানপাখি , আমার সন্তানের কাছে পিতা এবং অফিসে কর্মচারী এই যে আপনি একটা মানুষ এত্ত রূপে রূপায়িত এই বিষয়টায় পলিমরফিজম। ১৯৮৫ সালে স্যার পিটার ওয়েগনার এবং লুকা কার্ডেলি(Peter Wegner and Luca Cardelli) নামের একজন ইতালিয়ান কম্পিউটার প্রকৌশনলী যিনি মূলত অবজেক্ট থিওরী এর জন্য জনপ্রিয় পলিমরফিজম নামক কন্সেপ্টটা যুক্ত করেন সিমুলা (Simula) প্রোগ্রামিং ল্যাগুয়েজের সাথে ।&#x20;

source: [https://en.wikipedia.org/wiki/Polymorphism\_(computer\_science)](https://en.wikipedia.org/wiki/Polymorphism_\(computer_science\))

নিচে একটা উদাহরন দিয়ে বুঝানোর চেষ্টা করলাম।

```javascript
// Parent constructor function
function Animal(name) {
  this.name = name;
}

// Child constructor functions
function Dog(name) {
  Animal.call(this, name);
}

function Cat(name) {
  Animal.call(this, name);
}

// Shared method through prototype
Animal.prototype.speak = function() {
  console.log(`${this.name} makes a sound.`);
};

const dog = new Dog("Buddy");
const cat = new Cat("Whiskers");

dog.speak(); // Output: Buddy makes a sound.
cat.speak(); // Output: Whiskers makes a sound.

```

> কোনটা object আর কোনটা instance যাতে গুলিয়ে না জান একটা স্কিন শর্ট দিয়ে দিলাম কারন আমি এইটা এই এখানে খুব উচ্ছারণ করব।&#x20;
>
>

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

কোডটা লক্ষ্য করলে দেখবেন আমি এইখানে Animal নামে একটা কন্সট্রাক্টর ফাংশন বানিয়ে নিয়েছি পরে একটা Dog নামে ফাংশন কন্সট্রাক্টর বানিয়ে তাতে Animal ফাংশন টা কে কল করে নিয়েছি যাতে করে Animal ফাংশন টা Dog ফাংশনের পরিচয় নেয় সে জন্য তাতে this মানে Dog ফাংশন কে নির্দেশ করে দিয়েছি।  একই কাজ টা আমি Cat ফাংশনের ক্ষেত্রে ও করে দিয়েছি। পরে Animal.prototype দিয়ে আমি Animal ফাংশনটার prototype এ speak  নামে একটা ফাংশন যুক্ত করে দিয়েছি এবং পরে আমি Dog এবং Cat এর জন্য অবজেক্ট বানিয়ে নিয়েছি এবং সেই অবজেক্ট থেকে স্পিক নামে ফাংশন টা কল করেছি। নিচের মতো করে।&#x20;

```javascript
dog.speak(); // Output: Buddy makes a sound.
cat.speak(); // Output: Whiskers makes a sound.
```

সেইম কোড টা আপনি চাইলে ক্লাস দিয়েও করতে পারেন নিচের মতো করে ।

```javascript
// Parent class
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

// Child classes
class Dog extends Animal {
  constructor(name) {
    super(name);
  }
}

class Cat extends Animal {
  constructor(name) {
    super(name);
  }
}

const dog = new Dog("Buddy");
const cat = new Cat("Whiskers");

dog.speak(); // Output: Buddy makes a sound.
cat.speak(); // Output: Whiskers makes a sound.
```
