# রেগুলার ফাংশন (Regular Function)

রেগুলার ফাংশন হচ্ছে জাভাস্ক্রিপ্টের শুরু থেকে ব্যাবহৃত ফাংশন। রেগুলার ফাংশন লেখার Syntext হচ্ছে।&#x20;

```javascript
function NameOfFunction(){
  //statement
}
or
function NameOfFunction(argument){
  //statement
  return value
}
```

Example:

```javascript
function add(num1, num2) {
  this.sum = num1 * num2
  return sum
}
```

রেগুলার ফাংশনের যে জিনিস ব্যবহার করা যায় সেইটা হলো আপনি এইখানে <mark style="color:orange;">this</mark> keyword ব্যাবহার করতে পারবেন। এইখানে <mark style="color:orange;">this</mark> বলতে ঐ ফাংশনকে নির্দেশ করে। এবং <mark style="color:orange;">this</mark> দিয়ে এইখানে ফাংশন স্কোপ কে বুঝায়।&#x20;

তাছাড়া আপনি রেগুলার ফাংশন কে কন্সট্রাক্টর ফাংশন হিসেবে লিখতে পারবেন এবং প্রোটো টাইপ  ও ব্যাবহার করতে পারেন।&#x20;
