# রেগুলার ফাংশন (Regular Function)

রেগুলার ফাংশন হচ্ছে জাভাস্ক্রিপ্টের শুরু থেকে ব্যাবহৃত ফাংশন। রেগুলার ফাংশন লেখার Syntext হচ্ছেঃ-

```javascript
function nameOfFunction(){
  //statement
}
or
function nameOfFunction(argument){
  //statement
  return value
}
```

উদাহরণঃ&#x20;

```javascript
function add(num1, num2) {
  this.sum = num1 * num2
  return sum
}
```

রেগুলার ফাংশনের যে জিনিস ব্যবহার করা যায় সেইটা হলো আপনি এইখানে <mark style="color:orange;">this</mark> keyword ব্যাবহার করতে পারবেন। এইখানে <mark style="color:orange;">this</mark> বলতে ঐ ফাংশনকে নির্দেশ করে। এবং <mark style="color:orange;">this</mark> দিয়ে এইখানে ফাংশন স্কোপ কে বুঝায়।&#x20;

তাছাড়া আপনি রেগুলার ফাংশন কে কন্সট্রাক্টর ফাংশন হিসেবে ও  লিখতে পারবেন এবং prototype  ও ব্যাবহার করতে পারেন।&#x20;

উদাহরনঃ&#x20;

```javascript
function Cat(){}
const cat = new Cat();
cat.name = "Coco";

console.log(cat)


output: 
Cat {name: 'Coco'}
```

Prototype উদাহরনঃ

```javascript
// Constructor function for a basic Shape
function Shape(x, y) {
    this.x = x;
    this.y = y;
}

// Adding a method to the Shape prototype
Shape.prototype.displayCoords = function() {
    console.log(`Coordinates: (${this.x}, ${this.y})`);
};

// Constructor function for a Circle, inheriting from Shape
function Circle(x, y, radius) {
    // Call the parent constructor using 'call' to set 'this' appropriately
    Shape.call(this, x, y);
    this.radius = radius;
}

// Inherit from Shape's prototype
Circle.prototype = Object.create(Shape.prototype);

// Add a method specific to Circle
Circle.prototype.calculateArea = function() {
    return Math.PI * this.radius * this.radius;
};

// Create instances
const myShape = new Shape(10, 20);
const myCircle = new Circle(30, 40, 5);

// Call methods
myShape.displayCoords();   // Output: Coordinates: (10, 20)
myCircle.displayCoords();  // Output: Coordinates: (30, 40)
console.log(myCircle.calculateArea()); // Output: 78.53981633974483

```
