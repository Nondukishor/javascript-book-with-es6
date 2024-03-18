# ফেচ (fetch)

২০১৫ সালে  **XMLHttpRequest** এর উত্তরসূরি হিসেবে **fetch API** টা আনা হয় বর্তমানে এইটার জনপ্রিয়তা দিন দিন বৃদ্ধি পাচ্ছে আর সামনে পাবে আরো। বর্তমানে সব ব্রাউজারে এইটা সাপোর্ট করে এবং বিল্ড ইন হওয়ার কারণে খুব ভাল পারফর্মেন্স করছে।&#x20;

**কেন ব্যাবহার করব?**

উত্তর হচ্ছে আমরা ajax যা করতাম এইখানে টিক একই কাজ টায় করব তবে একটু সুন্দর ভাবে মানে প্রমিস হিসবে। fetch মূলত একটি Promise এবং এই প্রমিস টি মুলত দুইটি প্যারামিটার নেয়। fetch মুলত কোন রিমোট সার্ভার থেকে ডাটা রিসিভ এবং পাঠানোর কাজে ব্যাবহার করা হয়।&#x20;

চলুন সিন্ট্যাক্স টা দেখে নেই কিভাবে লিখতে হয়।

{% code overflow="wrap" lineNumbers="true" %}
```javascript
fetch('url')
  .then(response => {
    //handle response            
    console.log(response);
  })
  .then(data => {
    //handle data
    console.log(data);
  })
  .catch(error => {
    //handle error
  });
```
{% endcode %}

অথবা

{% code lineNumbers="true" %}
```javascript
fetch('url', {
  Method: 'POST',
  Headers: {
    Accept: 'application.json',
    'Content-Type': 'application/json'
  },
  Body: body,
  Cache: 'default'
}).then(response => {
    //handle response            
    console.log(response);
  })
  .then(data => {
    //handle data
    console.log(data);
  })
  .catch(error => {
    //handle error
  });
```
{% endcode %}

fetch এর দুইটি সিন্ট্যাক্স আছে নিচে দেখানো হলোঃ-

```javascript
fetch(resource)
fetch(resource, options)
```

একটা তে আপনি শুধুমাত্র resource এর লিঙ্ক দিবেন যেইটা মূলত শুধুমাত্র ডাটা ফেচ করার জন্য অথবা GET করার জন্য ব্যবহার করা হয়।&#x20;

আরেকটা হচ্ছে যখন সাথে কিছু বিশেষ অপশন দিয়ে ডাটা ফেচ করা হয় বা পাঠানো হয়। সেগুলো হতে পারে GET, POST, PATCH,PUT DELETE .. ইত্যাদি রিকুয়েস্ট।

চলুন কিছু উদাহরন দেখে নেই।&#x20;

উদাহরন-১ঃ-

```javascript
// Specify the API endpoint URL
const apiUrl = 'https://jsonplaceholder.typicode.com/posts';

// Make a GET request using fetch
fetch(apiUrl)
  .then(response => {
    // Check if the response was successful
    if (!response.ok) {
      throw new Error(`Network response was not ok: ${response.status}`);
    }
    return response.json();
  })
  .then(data => {
    // Process the fetched data
    console.log('Fetched data:', data);
  })
  .catch(error => {
    console.error('Error:', error);
  });

```

উদাহরন-২ঃ

```javascript
const apiUrl = 'https://jsonplaceholder.typicode.com/posts';

const postData = {
  userId: 1,
  title: 'This is a post',
  body: 'This is body and wring here about something about body"
};

// Configure the fetch options
const options = {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify(postData)
};

fetch(apiUrl, options)
  .then(response => response.json())
  .then(data => {
    console.log('Data created:', data);
  })
  .catch(error => console.error('Error:', error));
```
