# এন এফ ই (NFE)

NFE(Name Function Expression) বুঝার আগে চলুন একটু পিছনে যায়। আমারা জানি জাভাস্ক্রিপ্ট অবজেক্ট বলে একটা ডাটা টাইপ আছে। জাভাস্ক্রিপ্টে ফাংশন অবজেক্ট হিসবে কাজ করে । ফাংশন জাভাস্ক্রিপ্টে অনেকগুলো সুবিধা দিয়ে থাকে যেমন ফাংশনকে কল করা যায়। অবজেক্ট এর মতো করে ডাটা যুক্ত করা যায় এবং বাদ দেওয়া যায়।&#x20;

আরো গভীরে যাওয়ার আগে আমরা একটা উদাহরণ দেখে নিই চলুনঃ-

{% code lineNumbers="true" %}
```javascript
function codingJsBook(){
  console.log("The book is helpfull for javascript developer");
}
console.log(codingJsBook.name)
```
{% endcode %}

output:&#x20;

```
codingJsBook
```

উপরে আমি একটি ফাংশন লিখেছি এবং সে ফাংশনটা কল না করে আমি সেটার `name` প্রোপার্টিটা এক্সেস করেছি। তার মানে হলো আমরা যখন কোন ফাংশন লিখি সেইটা যে নামে লিখা হয় সে নামটা একটা প্রোপার্টি হিসেবে কাজ করে ।&#x20;

উপরের কোডটি চাইলে এইভাবেও লিখা যায় ।

<pre class="language-javascript" data-line-numbers><code class="lang-javascript"><strong>const codingJsBook = function(){
</strong>  console.log("The book is helpfull for javascript developer");
}
console.log(codingJsBook.name)
</code></pre>

output:&#x20;

```
codingJsBook
```

ফাংশনে নাম assign করার মাধ্যমে ফাংশনের একটা পরিচিতি দেওয়া হয়। যাতে করে পরে আমরা যে ফাংশন লিখেছি সেইটার নাম দেখে যাতে বুঝতে পারি। এই যে আমরা ফাংশনের নাম এক্সেস করছি আর ফাংশন নামটা প্রোপার্টি হিসেবে রাখছে এই পুরো বিষয়টাকে বলে contextual name। অবজেক্টে আমরা যে মেথড লিখি সে মেথড গুলোতেও contextual name বিষয়টা আছে।&#x20;

যেমনঃ-&#x20;

{% code lineNumbers="true" %}
```javascript
let book={
    codingJs(){
     console.log("The book is helpfull for javascript developer")
    }
  }
console.log(book.codingJs.name)
```
{% endcode %}

output:

```
codingJs
```

আমরা চাইলে জাভাস্ক্রিপ্টে নাম ছাড়াও ফাংশন লিখতে পারি। যাকে আমরা  anonymous ফাংশন  বলি। যেমনঃ-

```
let arr = [function () {}]; 
console.log(arr[0].name); 
```

output:

```
""
```

সেক্ষেত্রে আপনি নামের পরিবর্তে শুধু empty string পাবেন।&#x20;

{% code lineNumbers="true" %}
```javascript
function ask(question, ...handlers) {
  let isYes = confirm(question);

  for(let handler of handlers) {
    if (handler.length == 0) {
      if (isYes) handler();
    } else {
      handler(isYes);
    }
  }

}

// for positive answer, both handlers are called
// for negative answer, only the second one
ask("Question?", () => alert('You said yes'), result => alert(result));
```
{% endcode %}
