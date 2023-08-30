# প্রতিশ্রুতি(Promise)

{% code title="কলব্যাক যেভাবে লিখতাম " lineNumbers="true" %}
```javascript
function fetchData(callback) {
  setTimeout(() => {
    const data = 'Fetched data';
    callback(data);
  }, 1000);
}

fetchData((result) => {
  console.log(result);
});

```
{% endcode %}



{% code title="Promise এ যেভাবে লিখতে হবে" lineNumbers="true" %}
```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const data = 'Fetched data';
      resolve(data);
    }, 1000);
  });
}

fetchData()
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.error(error);
  });
```
{% endcode %}
