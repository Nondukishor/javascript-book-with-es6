<h1 align="center">সিনট্যাক্স নিয়ে  যত কথা।</h1>

জাভাস্ক্রিপ্ট একটি লুসলি টাইপ ল্যাঙ্গুয়েজ এইটি অন্যান্য ল্যাঙ্গুয়েজের মতো খুব বেশি case sensitive না এইটির কারনে অবস্য অনেক সময় প্রব্লেম ও পড়তে হয় । তবে "user stric" নামে literal expression ইউস করেলে অনেকটা স্ট্রিক্ট মুডে প্রোগ্রাম রান করানো যায় । তাই বলে ইন্টারনেট ধুম করে এখন সার্চ দিয়ে বইসো না আস্তে আমি এক্সাম্পল দেখাচ্ছি তারপর একটু বুঝে যত ইচ্ছা সার্চ দাও মজা আর মজা পাবেন শুধু। 

জাভাস্ক্রিপ্ট তিন রকম ভাবে আপ্লিকেশনে লিখা যায় 

```html
Fisrt Syntex:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Image validator</title>
</head>
<body>
   
    <script>
        console.log('Hello Bangladesh');
        //alert('Hello Bangladesh')
    </script>
</body>
</html>
```



```html
Second syntex:



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Image validator</title>
</head>
<body>
    <form>
        <input type="submit" onclick="return confirm('are you sure to upload picture')" />
        <!-- inner tag js write -->
    </form>
</body>
</html>

```



```html
Third syntex :

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Image validator</title>
</head>
<body>
    <form>
        <input type="file" name="image" id="image" multiple accept='image/*' >
    </form>
    <script src="index.js"></script><!-- js file include from spearate file with .js extenstion-->
</body>
</html>
```

```javascript
index.js file

console.log('Hello Bangladesh');
```

