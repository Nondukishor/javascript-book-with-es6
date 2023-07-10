# নন-প্রিমিটিভ ডাটা টাইপ

নন-প্রিমিটিভ ডাটা টাইপ বলতে আসলে যেইটা বুঝায় সেইটা হলো এইটা পরিবর্তন যোগ্য আপনি চাইলেই এইটার টাইপ পরিবর্তন করতে পারবেন। এইটা মুলত প্রিমিটিভ ডাটা টাইপের রেফারেন্স বহন করে। আপনি চাইলে একটা নন প্রিমিটিভ ডাটা টাইপে দুই বা ততোধিক ভিন্ন ভিন্ন ডাটা টাইপ ব্যাবহার করতে পারেন।

উদাহরনঃ&#x20;

```javascript
const myObject = {
                 name: "Nipu",
                 height: 5.6,
                 age: 27,
                 canSwime: true,
                 skill: ["javascript", "PHP", "java", "python", "rust"],
                 }
                 
```

উপরের উদাহরণে দেখতে পাচ্ছেন আমি myObject এ ভিন্ন ভিন্ন ডাটা টাইপ ব্যাবহার করেছি। এখন আমারা যদি দেখতে চাই এর ডাটা টাইপ কি? তার জন্য আমাদের typeof নামে একটা বিল্ড ইন কি-ওয়ার্ড আছে সেইটা ব্যভার করা লাগবে।&#x20;

```javascript
typeof myObject
```

output:

```
'object'
```

&#x20;দেখতেই পাচ্ছেন আমরা এর ডাটা টাইপ পেলাম অবজেক্ট ।&#x20;

এখন আমরা যদি এর কোন ডাটা টাইপ value পরিবর্তন করতে চাই সেইটা ও করতে পারব যেমনঃ -

```javascript
myObject.name= "Nipu Chakraborty"
console.log(myObject)
```

output:

<pre class="language-javascript"><code class="lang-javascript"><strong>{
</strong>    "name": "Nipu Chakraborty",
    "height": 5.6,
    "age": 27,
    "canSwime": true,
    "skill": [
        "javascript",
        "PHP",
        "java",
        "python",
        "rust"
    ]
}
</code></pre>
