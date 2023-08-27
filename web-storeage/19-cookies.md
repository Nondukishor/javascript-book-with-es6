# কুকিস(Cookies)

```
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
