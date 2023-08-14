# ইফি(IIFE)

IIFE এর পুরো নাম হলো (Immediately Invoked Function Expression)। এই এর আসলে নাম হওয়া উচিত ছিল আমার মাঝে মাঝে মনে হয় **anonymous self-invoking function** কারন এইটা আসলে একটা নাম ছাড়া ফাংশন কে কল করে যা আপনার কল করা লাগবে না মানে হলো সে নিজেই নিজেকে কল করে আরকি।&#x20;

```javascript
(function () {
    console.log("Hello I am IIFE");
})()
```

