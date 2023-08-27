# সেশন (Session)

**সেশনঃ**  Browser ওপেন হওয়ার পর যখন ই আমারা একটা ওয়েভ সাইটে ল্যান্ড করি, তখন ব্রাউজারে একটা সেশন ওপেন হয়, আর প্রতিবার যখন ই ট্যাব ক্লোজ করে দেই সেশন নষ্ট হয়ে যায় । আমরা যদি একি url এর আলাদা আলাদা ট্যাব ও খুলি সে ক্ষেত্রেও ব্রাউজার আলাদা আলাদা সেশন করে নেয়। এইটা অনেকটা আলাদা ফ্ল্যাট এর  মতো করে কাজ করে ঐ ফ্ল্যাটে যা আছে তা ঐ ফ্ল্যাটের এমনকি একিরকম ফ্ল্যাট হলেও ফ্ল্যাটের যা আছে সবই আলাদা সবই ইউনিক।&#x20;

```
window.sessionStorage
```

or just

```
sessionStorage
```

Javascript এ sessionStorage নামে একটা বিল্ড ইন অব্জেক্ট আছে যার মাধ্যমে আপনি চাইলেই সেশন নিয়ে যাবতীয় কার করতে পারেন। যেমন store করা delete/remove করা এবং get করা&#x20;

চলুন কিছু উদাহরন দেখে নেই।&#x20;



সেশন স্টোরে ডাটা সেভ করা&#x20;

```
sessionStorage.setItem("key", "value");
```

সেশন স্টোর থেকে ডাটা গেট করা&#x20;

```
sessionStorage.getItem("key");
```

সেশন স্টোর থেকে ডাটা রিমুভ করা বা ডিলেট করা

```
sessionStorage.removeItem("key");
```

সেশন স্টোর থেকে ডাটা সব ক্লিয়ার করা&#x20;

```
sessionStorage.clear();
```

কিছু উদাহারন দেখে নেওয়া যাক।&#x20;

```html
<!DOCTYPE html>
<html>
<head>
  <title>Client-side Session Example</title>
</head>
<body>
  <button id="loginBtn">Login</button>
  <button id="logoutBtn">Logout</button>
  <div id="profile"></div>

  <script>
    // Function to set session data
    function setSession(key, value) {
      sessionStorage.setItem(key, value);
    }

    // Function to get session data
    function getSession(key) {
      return sessionStorage.getItem(key);
    }

    // Function to clear session data
    function clearSession(key) {
      sessionStorage.removeItem(key);
    }

    // Function to handle login
    function handleLogin() {
      setSession('username', 'johnDoe');
      updateProfile();
    }

    // Function to handle logout
    function handleLogout() {
      clearSession('username');
      updateProfile();
    }

    // Function to update profile information
    function updateProfile() {
      const profileDiv = document.getElementById('profile');
      const username = getSession('username');

      if (username) {
        profileDiv.innerHTML = `Welcome, ${username}!`;
      } else {
        profileDiv.innerHTML = 'Please log in.';
      }
    }

    // Attach event listeners
    const loginBtn = document.getElementById('loginBtn');
    const logoutBtn = document.getElementById('logoutBtn');

    loginBtn.addEventListener('click', handleLogin);
    logoutBtn.addEventListener('click', handleLogout);

    // Initial profile update
    updateProfile();
  </script>
</body>
</html>

```

আপনি session কোথায় কোথায় ব্যাবহার করতে পারেন?&#x20;

* User Authentication
* User Authorization
* Shopping cart
* From data Persistence
* User Preference and settings
* User activity Tracking
* Mutli step Workflow
* Caching Data
* tempory CSRF token
