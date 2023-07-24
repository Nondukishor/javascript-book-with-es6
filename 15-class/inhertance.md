# ইনহেরিটেন্স (Inhertance)

```javascript
class Country {
  constructor(name) {
    this.countryName = name;
  }
  getCountryName() {
    return 'Country Name: ' + this.countryName;
  }
}

class Division extends Bangladesh {
  constructor(country,division) {
    super(country);
    this.division = division;
  }
  show() {
    return 'Country: 'this.getCountryName() + "division: " + this.division;
  }
}

let myDivision = new Division("Bangladesh", "Chittagong");
console.log(myDivision.show());
```
