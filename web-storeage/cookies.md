# বিস্কিটের টুকরো (Cookies)

**বিস্কুট এর টুকরা আর ওয়েভ এর গল্প।**

১৯৯৪ সালে মানে আমার জন্মের প্রায় দুই বছর আগে নেটস্কেপের একজন গুনী প্রোগ্রামার স্যার **লু মন্টুলি** Lou Montulli ওয়েভ ব্রাউজারে সর্বপ্রথম যুক্ত করে। এর পিছনে গল্প ছিল এইটা যে তারা ই- কমার্স এর কেনা কাটার জন্য ডাটা গুলো একটা জায়গায় সংরক্ষন করবে তাও আবার ব্রাউজারে।&#x20;

১৯৯৫ সালে তিনি তার এই আবিষ্কারকে প্যাটেন্ট করেন কুকিস টেকনোলজি নামে। এবং একই সময়ে তিনি কুকিসের ভার্সন ২ ইন্টারনেট এক্সপ্লোর এর সাথে বাজারে নিয়ে আসেন।&#x20;

১৯৯৬ সালে কুকিস কে ফিন্যান্সিয়াল টাইম সুরক্ষিত নয় বলে ঘোষনা দেয়। আবার এইটা নিয়ে কাজ শুরু হয় এবং

১৯৯৭ সালে ব্লক থার্ড পার্টি কুকিস নামে একটা বৈশিষ্ট্য যুক্ত করে আবার বাজারে ছাড়া হয় এবং সর্বশেষ ১৯৯৮ সালে মানে আমি যখন হাঁটি হাঁটি পা পা তখন ইন্টারনেট  এক্সপ্লোর একে সুরক্ষিত বলে ঘোষণা দেয়।&#x20;

ইতিহাসের গল্পটাকে চিত্রায়িত করা হলো &#x20;

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>কুকিস ইতিহাস </p></figcaption></figure>

```javascript
<!DOCTYPE html>
<html>
<head>
  <title>Cookie Example</title>
</head>
<body>
  <button id="setCookieBtn">Set Cookie</button>
  <button id="getCookieBtn">Get Cookie</button>
  <button id="deleteCookieBtn">Delete Cookie</button>
  <div id="output"></div>

  <script>
    // Function to set a cookie
    function setCookie(name, value, days) {
      const expires = new Date();
      expires.setTime(expires.getTime() + (days * 24 * 60 * 60 * 1000));
      document.cookie = `${name}=${value};expires=${expires.toUTCString()};path=/`;
    }

    // Function to get a cookie by name
    function getCookie(name) {
      const cookieArray = document.cookie.split('; ');
      for (const cookie of cookieArray) {
        const [cookieName, cookieValue] = cookie.split('=');
        if (cookieName === name) {
          return cookieValue;
        }
      }
      return null;
    }

    // Function to delete a cookie by name
    function deleteCookie(name) {
      setCookie(name, '', -1);
    }

    // Function to update the output
    function updateOutput(message) {
      const outputDiv = document.getElementById('output');
      outputDiv.textContent = message;
    }

    // Attach event listeners
    const setCookieBtn = document.getElementById('setCookieBtn');
    const getCookieBtn = document.getElementById('getCookieBtn');
    const deleteCookieBtn = document.getElementById('deleteCookieBtn');

    setCookieBtn.addEventListener('click', () => {
      setCookie('username', 'johnDoe', 7);
      updateOutput('Cookie "username" set.');
    });

    getCookieBtn.addEventListener('click', () => {
      const username = getCookie('username');
      if (username) {
        updateOutput(`Cookie "username" value: ${username}`);
      } else {
        updateOutput('Cookie "username" not found.');
      }
    });

    deleteCookieBtn.addEventListener('click', () => {
      deleteCookie('username');
      updateOutput('Cookie "username" deleted.');
    });
  </script>
</body>
</html>

```

কুকিসের ব্যাবহারঃ

১। Session Management

২। Personalization

৩। Shopping Carts

৪। User Tracking and Analytics

৫। Remember Me Functionality

৬। Ad Tracking and Targeting

৭। Security

৮। User Experience Enhancement

৯। Localization
