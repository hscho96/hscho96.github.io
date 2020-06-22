---
layout: post
title: "Nodejs - Various Operators"
date: 2020-06-20 21:47:13 +0800
categories: Nodejs
tags: Javascript Nodejs
---


## Variable and Constant

We can declare variable with `let`, ex) let fruit1 = 'apple';
In addition, constant can be declared with `const`, ex) const pi = 3.14;

The variable declared with `let` can be changed into another value if we want, however the constant declared with `const` is not changeable.

## Array
There are typically two ways in declaring Array. `1. using [] , 2. using new Array()`

{% highlight ruby %}
const numbers = [1,2,3];
const strings = ['hello', 'bye', 'welcome'];

const numbers 2 = new Array(1, 2, 3);
const stings 2 = new Array('hello', 'bye', welcome);
{% endhighlight %}

You can insert values in array like this

{% highlight ruby %}
const arrNumbers = [];
arrNumbers.push(1);
arrNumbers.push(2);

const arrTexts = [];
arrTexts.push('hello', 'welcome');
{% endhighlight %}

## How to check the type of Variables
we can easily check the type of variables with using `typeof`.
{% highlight ruby %}
const pi = 3.14;
const name = 'James';
console.log('pi : %s', typeof pi); // pi : number
console.log('name : %s', typeof name); // name : string
console.log('[] : $s', typeof []); // []: object
{% endhighlight %}

## True / False Boolean expression

{% highlight ruby %}
console.log('10 > 20:' , 10 > 20); // 10 > 20 : false
console.log('30 > 20: , 30 > 20); // 30 > 20 : true

console.log('typeof (true): ', typeof(true)); // typeof (true): boolean
console.log('typeof (false): ', typeof(false)); // typeof (false): boolean


{% endhighlight %}

## Comparison Operator

It is important to known the difference between `==` and `===`.  
`==` just compares the values between two variables, however `===` not only compares the values but also the types of the variables.

{% highlight ruby %}
const a = 5;
const b = 6;

if (a == 5 ){
  console.log(a == 5); // true
  console.log(a == b); // false
  console.log(a == '5') // true
}

if (a === 5 ){
  console.log(a === 5); //true
  console.log(a === b); //false
  console.log(a === '5'); //false -> equal values, but not equal type
}

if (a > b ){
  console.log(a > b); // print nothing
}

if (a < b ){
  console.log(a < b); //true
}

if (a >= 5 ){
  console.log(a >= 5); //true
  console.log(a >= b); //false
}

if (a <=5 ){
  console.log(a <= 5); //true
  console.log(a <= b); //true
}
{% endhighlight %}

## Ternary Operator
`<condition> ? <when it's true> : <when it's false> `

{% highlight ruby %}
const num1 = 1;
const num2 = 2;
const result = num1 > num2 ? 'num1' : 'num2';
console.log(result, 'is bigger'); // num2 is bigger
{% endhighlight %}
