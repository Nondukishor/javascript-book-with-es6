<h1 align="center"> ফাংশন </h1>
ফাংশন মানে হলো কাজ। আমাদের দৌনিক কাজে ফাংশন বা কাজটা কত বড় কেমন হবে সেটা নির্ণয় করা কঠিন হলেও প্রোগ্রামিং এর ক্ষেত্রে এইটা  একটু ভিন্ন এখানে আপনি নির্ধারন করে দিতে পারবেন কোন ফাংশন কতটুকু কাজ করবে। বড় কাজ গুলো ছোট ছোট ফাংশন ভাগ করে নিতে পারবেন  এবং সে কাজ গুলোকে বার বার ব্যবহার উপযোগী ও করে তুলতে পারবেন। একসময় জাভাস্ক্রিপ্ট শুধু মাত্র ফাংশন বেইস ল্যাংগুয়েজ ছিল। একমাস্ক্রিপ্ট আশার পর এতে ক্লাস যোগ করা হয় তবে বেবেল এর মাধ্যমে যদি আপনি সেটা লক্ষ করেন তাহলে দেখতে পাবেন মুলত তাও ফাংশন দিয়ে তৈরি করা। 

এই অধ্যায়ে আমরা যেটা মূলত  জানার চেষ্টা করব সেটা হলো 

১। ফাংশন কি? এবং কিভাবে ফাংশন লিখা যায়? 

২। অ্যারো ফাংশন কি? কিভাবে লেখা যায় ? এবং এবং এর সুবিধা কি?

৩। কন্সট্রাক্টর ফাংশন কি?

৪। রিটান টাইপ ফাংশন?

৫। ফাংশন এর মাঝে আরগুমেন্ট বা প্যারামিটার পাস করা।

 <h1 align="center">ফাংশন কি? এবং কিভাবে ফাংশন লিখা যায়?</h1>
ফাংশন মানে যে কাজ সেটা আগেই বলেছি।অর্থাৎ বড় বড় প্রোগ্রামের কোন নির্দিষ্ট কাজ কে ছোট ছোট কাজে ভাগ করে নেওয়াকে ফাংশন বলে। এবার আসেন একটু দেখে নেই কিভাবে ফাংশন লিখতে হবে। 

syntex:-

```javascript
//regular function syntex:
function nameOfFunction(argument){
//statement
    return something;
}
//arrow function syntex:
const nameofFunction=(argument)=>{
  //statement
    return something;
}
```

প্যারামিটার ও রিটার্ন টাইপের উপর ভিত্তি করে ফাংশন চার ভাগে ভাগ করা যায়। যথাঃ-

**১। Fuction without Argument  and no return.**

**2। Function with Argument and no return.**

**৩। Function with Argument and return.**

**৪। Function without argument but return.**

 **Fuction without Argument  and no return:-** এইধরনের ফাংশনের ক্ষেত্রে কোন আরগুমেন্ট থাকে না এবং কোন রিটার্ন ভ্যালু ও থাকে না।

example:

```javascript
//function define

function isAdult(){
let age=18;
if(age>17){
  console.log("Yeah!, you are adult.")
 }
}

isAdult()//function call
```

এই ফাংশন এর মধ্যে আপনি লক্ষ্য করলে দেখতে পাবেন যে এইখানে কোন আরগুমেন্ট নাই এবং ফাংশনটা কোন কিছু রিটার্ন ও করতে পারছে না।

**Function with Argument and no return:-** এই ধরনের ফাংশনের ক্ষেত্রে আরগুমেন্ট থাকেলেও কো রিটান ভ্যালু থাকে না।

example:

```javascript
//function define
function isAdult(age){
   if(age>17){
     console.log("yeah! you are adult")
   }
}

isAdult(18); //function call and argumant passing
```

এই ফাংশনটা লক্ষ্য করলে দেখা যায় এতে একটি আর্গুমেন্ট আছে কিন্ত কোন রিটার্ন ভ্যালু নাই। 

**Function with Argument and return:** function with argument and return টাইপের ফাংশনের ক্ষেত্রে ফাংশনের আরগুমেন্ট ও থাকে রিটার্ন ও থাকে । নিচে উদাহরনটি লক্ষ্য করুন।

```
//function define 
function result(subject,gpa){
  return subject+":"+ gpa
}

result('Bangla',"5:00"); // function call


```

