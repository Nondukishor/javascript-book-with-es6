# পলিমরফিজম (Polymorphism)

পলিমরফিজম (Polymorphism) বা বহুরূপতা একটি গ্রিক্ শব্দ যার অর্থ একাধিক আকার গ্রহণ করার ক্ষমতা। &#x20;

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
