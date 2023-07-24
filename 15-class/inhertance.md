# ইনহেরিটেন্স (Inhertance)

ইনহেরিটেন্স এর মানে হচ্ছে উত্তরাধিকার সূত্রে পাওয়া। যদি বলি পুত্র/কন্যা তার বাবা/মায়ের কিছু বৈশিষ্য পেয়ে থাকে যেইটা উত্তরাধিকার সূত্রেই পেয়ে থাকে সেইটাই ইনহেরিটেন্স । আরো যদি সরল ভাবে বলি একটা বস্তু বা একটা জিনিস বা একটা অবজেক্ট যখন অন্য একটা অবজেক্ট বা অন্য একটা বস্তু বা অন্য একটা জিনিস থেকে কিছু বৈশিষ্ট্য ধার করে বা নিজের মধ্যে নিয়ে নেয় সেইটায় ইনহেরিটেন্স । &#x20;

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>ইনহেরিটেন্স </p></figcaption></figure>

নিচে একটা উদাহরন দিয়ে দেখানো হলো।

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
    return 'Country: ' + this.getCountryName() + "division: " + this.division;
  }
}

let myDivision = new Division("Bangladesh", "Chittagong");
console.log(myDivision.show());
```

