---
description: >-
  সতর্ক বার্তাঃ কেউ যদি বইটির কোন অংশ খারাপ উদ্দেশ্যে বা বাণিজ্যিক উদ্দেশ্য
  ব্যবহার  করে তাহলে কপিরাইট আইন অন্তর্ভুক্ত সকল প্রকার প্রক্রিয়া অনুসরণ করতে
  বাধ্য থাকব।
---

# সিনট্যাক্স নিয়ে যত কথা।

জাভাস্ক্রিপ্ট একটি কম কড়াকড়ি মানে (loosely) টাইপ ল্যাঙ্গুয়েজ।এইটি অন্যান্য ল্যাঙ্গুয়েজের মতো খুব বেশি case sensitive না। এটার কারণে অবশ্য অনেক সময় বিপাকে  পড়তে হয় । তবে **"use strict"** নামে **literal expression** ব্যবহার করলেও অনেকটা **strict mode** প্রোগ্রাম রান করানো যায় । জাভাস্ক্রিপ্ট তিন রকম ভাবে লিখা যায়।

1. **Inner Script**
2. **Inline Script**
3. **External Script File**



#### **Inner Script**

{% code title="inline-script.html" overflow="wrap" lineNumbers="true" %}
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> প্রথম প্রোগ্রাম হ্যাঁলো বাংলাদেশ </title>
</head>
<body>
    <script>
        console.log('হ্যাঁলো বাংলাদেশ');
    </script>
</body>
</html>
```
{% endcode %}

{% hint style="info" %}
১। প্রথমে একটা .html extension যুক্ত ফাইল বানানো হয়েছে। নাম দেওয়া হয়েছে **inline-script.html**

২। HTML-5 এর বেসিক কিছু কোড লিখা হয়েছে।

৩। ১৩ নং লাইনে script নামে একটা ট্যাগ যুক্ত করা হয়েছে ।&#x20;

৪। script ট্যাগ এর ভিতরে `console.`<mark style="color:purple;">`log`</mark>`('হ্যাঁলো বাংলাদেশ'); কোডটা লিখা হয়েছে।`

`৫। ব্রাউজার দিয়ে ফাইলটাকে open করা হয়েছে।`&#x20;
{% endhint %}

**Output:**

```sh
হ্যাঁলো বাংলাদেশ
```

#### Inline Script

{% code title="inline-script.html" overflow="wrap" lineNumbers="true" %}
```html
Second syntex:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> দ্বিতীয় প্রোগ্রাম আমি তোমায় ভালবাসি </title>
</head>
<body>
    <form>
        <button onclick="return confirm('আমি তোমায় ভালবাসি')">
           ক্লিক করে জেনে নিন  
        </button>
        <!--javascript in inner tag -->
    </form>
</body>
</html>

```
{% endcode %}

{% hint style="info" %}
১। প্রথমে inline-script.html নামে একটা ফাইলে বানানো হয়েছে।&#x20;

২। তারপরে HTML-5 এর বেসিক কিছু কোড লিখা হয়েছে ।

৩। body ট্যাগ এর ভিতরে form ট্যাগ যুক্ত করে তাতে আরেকটা button ট্যাগ যুক্ত করা হয়েছে।

৪। button ট্যাগ এর ১৩ নং লাইনের মতো করে onclick এট্রিভিউটে একটা কোড যুক্ত করা হয়েছে `onclick="return confirm('আমি তোমায় ভালবাসি')"`

৫। সব শেষে আগের মতো করে ব্রাউজারে open করা হয়েছে।

৬। **ক্লিক করে জেনে নিন button** টাতে ক্লিক করলে একটা মেসেস দেখাবে **আমি তোমায় ভালবাসি**
{% endhint %}

#### **External Script File:**

{% code title="index.html" overflow="wrap" lineNumbers="true" %}
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> তৃতীয় প্রোগ্রাম বাংলাদেশ সবুজ শ্যামল দেশ  </title>
</head>
<body>
  <script src="external-script.js"></script>
</body>
</html>
```
{% endcode %}

{% code title="external-script.js" overflow="wrap" lineNumbers="true" %}
```javascript
console.log('বাংলাদেশ সবুজ শ্যামল দেশ');
```
{% endcode %}

{% hint style="info" %}
১। প্রথমে একটা index.html নামে ফাইল বানিয়ে নেওয়া হয়েছে এবং আগের মতো করে বেসিক HTML-5 এর কিছু কোড লিখে নেওয়া হয়েছে।&#x20;

২। ১০ নং লাইনের মতো করে script যুক্ত করা হয়েছে এবং তাতে src নামে যে এট্রিবিউট আছে সেটাতে আমাদের **external-script.js** ফাইলটি যুক্ত করে দেওয়া হয়েছে।&#x20;

৩। **external-script.js** নামে ফাইল করে তাতে _`console.log('বাংলাদেশ সবুজ শ্যামল দেশ');`_ কোডটি লিখা হয়েছে।&#x20;

৪। পরে ব্রাউজার দিয়ে আগের মতো করে open করা হয়েছে।&#x20;

৫। ব্রাউজারে কনসোল open করলে দেখা যাবে _**`বাংলাদেশ সবুজ শ্যামল দেশ`**_ লিখা দেখা যাচ্ছে।&#x20;
{% endhint %}

এখন আপনার কাজ হচ্ছে আপনি এইরকম আরো কিছু প্রোগ্রাম লিখবেন যেখানে আপনি আপনার প্রিয় দুইজন মানুষ এবং আমাদের দেশকে নিয়ে লিখবেন। তো শুরু করে দিন আর লিখা শেষ হলে আমাকে মেইল করে জানিয়ে দিন pro.nipu@gmail.com এই মেইলে মাধ্যমে।
