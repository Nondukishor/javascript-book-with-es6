# জিওলোকেশন এপি আই (Geolocation API)

## জিওলোকেশন এপি আই কি?

HTML 5 এর পর থেকেই মূলত জিওলোকেশন এপি আই এর এপি আই দেওয়া হয় জাভাস্ক্রিপ্টে। এইটি মূলত জেটি মূলত ইউজারের লোকেশন এক্সেস প্রদান করে থাকে। চলুন  দেখে নেই জিওলোকেশন এপি আই কিভাবে ব্যাবহার করেঃ-

```javascript
if (navigator.geolocation) {
  navigator.geolocation.getCurrentPosition(function(position) {
    const latitude = position.coords.latitude;
    const longitude = position.coords.longitude;
    console.log("Latitude: " + latitude + " Longitude: " + longitude);
  });
} else {
  console.log("Geolocation is not supported by this browser.");
}
```

&#x20;



```javascript
const watchId = navigator.geolocation.watchPosition(successCallback, errorCallback);
// To stop watching location
navigator.geolocation.clearWatch(watchId)
```
