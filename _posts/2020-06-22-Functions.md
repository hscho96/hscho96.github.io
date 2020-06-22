---
layout: post
title: "Nodejs - Functions"
date: 2020-06-22 00:16:13 +0800
categories: Nodejs
tags: Javascript Nodejs
---
## Declaring Functions
We can declare functions in different ways.
{% highlight ruby %}
//This is function declaration (함수 선언식)
function printMessage(message) {
  console.log(message);
}

//This is function expression (함수 표현식)
const printWelcome = function () {
  console.log('welcome');
}

printMessage('bye');
printWelcome();

//If we check the type of each function with `typeof`, we can see they are functions.
console.log('typeof printMessage : %s', typeof printMessage);
console.log('typeof printWelcome : %s', typeof printWelcome);

//Another way of declaring function with pre-declared function above.
const pm = printMessage;
pm('good morning');
console.log('typeof pm : %s', typeof pm);
{% endhighlight %}

This is a new function called `arrow function` developed in ES6 to omit `function`, `return` when we declare functions.
{% highlight ruby %}
const printHello = () => console.log('hello');
const printHello2 = () => 'hello2'; //return hello2
const printMessage = message => console.log(message);
const plus = (a, b) => a+ b;

const sumAndPrint = (a, b) =>{
  const result = a + b;
  return `result is ${result}`;
}

const result = sumAndpRINT(10,20);
console.log(result);
{% endhighlight %}
## Function as Parameter
Another interesting element in function in `node.js` is that function can be used as variable.
{% highlight ruby %}
//declare plus function
function plus(a, b) {
 return a + b;
}

//declare p as plus function
let p = plus;

//This is a function that takes function as parameter
function calculate(a, b, func){
  return func(a, b);
}

//calcualte the result by passing plus function as parameter.
console.log(calculate(10, 20, plus));
{% endhighlight %}
## Callback Functions
Callback function literally callbacks function that is previously declared.
It is called `Chaining` because of its property.
{% highlight ruby %}
const sum = (a, b) => a + b;

const printResult = (result) => {
  console.log(`result is ${result}.`);
};

const calculateAndPrint = (calculationResult, callback) => {
  callback(calculationResult);
};

calculateAndPrint(sum(10, 20), printResult);
{% endhighlight %}
