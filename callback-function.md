# কলব্যাক ফাংশন (callback function)

কলব্যাক ফাংশন জিনিসটা হলো একটা ফাংশনের ভিতরে আরেকটা ফাংশন আরগুমেন্ট হিসেবে দেওয়া হয় এবং সে ফাংশন টি ঐ ফাংশনের ভিতরে কাল করা হয় । এই পদ্ধতি ব্যাবহার করে একটা ফাংশন দিয়ে অন্য একটা ফাংশন কে কল করা যায়।&#x20;

গল্পঃ&#x20;

আপনারা নিশ্চয় আখের জুস খেয়েছেন। আর যদি খেয়ে থাকেন নিশ্চয় দেখেছেন আখের জুস বানানোর মেশিন ধরে নেই যে আখের মেশিনটা হচ্ছে সে একটা ফাংশন সেখানে আমি আখ দিব ধরে নিলাম আখ হচ্ছে কলব্যাক ফাংশন। যে মেশিনের ভিতরে গিয়ে কল হবে এবং প্রসেস হবে আর পরিবর্তে জুস দিবে। কলব্যাক ফাংশন টা ও এমন একটা বিষয়।&#x20;

এখন কথা হচ্ছে আমি কেন এই কল ব্যাক ফাংশন ব্যাবহার করব ?

ধরুন আপনার একটা কাজ আছে যেইটা আপনি করতে চাইছেন না মানে আপনি অনেক অনেক ব্যাস্ত। এখন আপনি সিদ্ধান্ত নিলেন আপনি কাজ আপনি অন্য কারো হাতে করিয়ে নিবেন কিন্তু আপনার অফিসে বসেই করে করে দেওয়া লাগবে বাইরে গিয়ে করলে হবে না এছাড়া আপনি চাইছেন সেই কাজ টা করবে টিকই কিন্তু যদি আপনার অফিসের আইপি ও পিসি ব্যাবহার করে তখন আসলে এমন কিছু শর্ত জুড়ে দিয়ে আপনি বাইরের মানুষটাকে দিয়ে আপনার কাজ টা আপনার অফিসেই করিয়ে নিলেন এমন বিষয় হলে আসলে কলব্যাক ফাংশন ব্যাবহার করা হয়।&#x20;

আসুন এবার একটি জীবন থেকে নেওয়া উদাহরণ দেখিঃ

```javascript
function servent(office_ip, ip, current_location, office_location, work){
  if(ip===office_ip && current_location===office_location){
    console.log(`you are authorized to work: ${work}`)
  }
  else{
    console.log(`you are not authorized to work: ${work}`)
  }
}

function Office(worker){
  const office_ip = "198.168.1.1"
  const ip="198.168.1.1"
  const current_location = "Dhaka"
  const office_location="Dhaka"
  const work = "Print file"
  worker(office_ip, ip, current_location, office_location, work)
}


Office(servent)
```

আশা করি বুঝে গেছেন কলব্যাক ফাংশন কি এবং কেন লিখতে হয়। এখন আমরা দেখব আসলে কলব্যাক ফাংশন দিয়ে আসলে আমরা কি ধরণের সমস্যার সমাধান করতে পারি। তার আগে একটা কোড লিখে নেই।

```javascript
function calculator(number1, number2, callbackFn){
   return callbackFn(number1, number2)
}

function sum(number1, number2){
  return number1 +number2
}

function sub(number1, number2){
  return number1 - number2
}

function div(number1, number2){
  return number1 / number2
}

function mul(number1, number2){
  return number1 * number2
}

const result1 = calculator(1, 2, sum) //output: 3
const result2 = calculator(1, 2, sub) //output: -1
const result3 = calculator(1, 2, div) //output: 0.5
const result4 = calculator(1, 2, mul) //output: 2
```

উপরের কোড গুলো লক্ষ্য করলে দেখবেন এইখানে আসলে কোন ফাংশনে যে ডাটা টা দেওয়া হচ্ছে সে ডাটার উপর ভিত্তি করে ভিন্ন ভিন্ন সময়ে ভিন্ন অপারেশনের প্রয়োজন পরে আর এইসব ধরনের সমস্যা সমাধনের জন্যই মুলত কলব্যাক ফাংশনের উদ্ভব হয়েছে। বিষয়টা মজার।&#x20;

#### কলব্যাক হেল কি?

কলব্যাক হেল এমন একটা বিষয় যেইটা Pyramid of Doom তৈরি করে। কথাটা শুনে একটু নতুন লাগলেও আমরা আস্তে আস্তে এইটা বুঝার চেষ্টা করব। চলুন একটা কোড দেখে নেই&#x20;

{% code title="Pyramid-doom.js" overflow="wrap" lineNumbers="true" %}
```javascript
fun1(function(value1){
   fun2(function(value2){
      fun3(function(value3){
         fun4(function(value4){
            func5(function(value5){
              func6(fuction(value6){
                console.log(value6)
             })
           })
         })
      })
   })
})
```
{% endcode %}

এই যে কোড টা দেখছেন এইটা কিন্তু দেখতে অনেকটা পিরামিড এর মতো লাগছে তাই না আর এইটা তৈরি হয়েছে নেস্টেড কলব্যাক এর কারণে।&#x20;

আর এই যে নেস্টেড কোডটা তৈরি হলো এইটায় মূলত হচ্ছে কলব্যাক হেল।&#x20;
