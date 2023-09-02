# অবস্ট্রাক্শন(Abstraction)



```javascript
class Car {
  constructor(make, model) {
    this.make = make;
    this.model = model;
  }

  start() {
    console.log(`${this.make} ${this.model} is starting.`);
  }
}

const myCar = new Car('Toyota', 'Camry');
myCar.start();
```
