# ইনহেরিটেন্স (Inhertance)

ইনহেরিটেন্স এর মানে হচ্ছে উত্তরাধিকার সূত্রে পাওয়া। যদি বলি পুত্র/কন্যা তার বাবা/মায়ের কিছু বৈশিষ্ট্য পেয়ে থাকে যেইটা উত্তরাধিকার সূত্রেই পেয়ে থাকে সেইটাই ইনহেরিটেন্স । আরো যদি সরল ভাবে বলি একটা বস্তু/জিনিস/একটা অবজেক্ট যখন অন্য একটা অবজেক্ট বা অন্য একটা বস্তু বা অন্য একটা জিনিস থেকে কিছু বৈশিষ্ট্য ধার করে বা নিজের মধ্যে নিয়ে নেয় সেইটায় ইনহেরিটেন্স।

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p>ইনহেরিটেন্স </p></figcaption></figure>

ছবি রেফারেন্সঃ [https://seleniumautomationtester.wordpress.com/2017/03/09/inheritance-in-java/](https://seleniumautomationtester.wordpress.com/2017/03/09/inheritance-in-java/)

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

class Division extends Country {
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

উপরের উদাহরণ টা যদি লক্ষ্য করেন তাহলে দেখতেই পাচ্ছেন **Country,Division** নামে দুইটি ক্লাস লিখেছি এবং একটা আরেকটা কে <mark style="color:orange;">extends</mark> keyword দিয়ে  **Division** ক্লাসে আমি **Country** ক্লাসটিকে ইনহেরিট করেছি এবং তারপরে কন্সট্রাটর ক্লাসে super ফাংশন্টাকে কল করেছি এবং **Country** ক্লাসের কন্সটাক্টর ফাংশন এর দিকে লক্ষ্য করলে দেখবেন সেখানে একটা প্যারামিটার নিচ্ছে আর সেইটা getCountryName নামের ফাংশন টি দিয়ে দেখানো হচ্ছে তাই আমি যখন super ফাংশন টা কে কল করছি তখন এর মাঝে country প্যারামিটার টা পাঠিয়ে দিচ্ছি।&#x20;
