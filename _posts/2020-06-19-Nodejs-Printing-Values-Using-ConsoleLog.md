---
layout: post
title:  "Nodejs - Printing Values using console.log"
date:   2020-06-19 22:47:13 +0800
categories: Nodejs
tags: Javascript Nodejs
---

console.log shows the result of the program



you can run the program using "Ctrl + Shift + B"
{% highlight c linenos %}
console.log('hello');
{% endhighlight %}

in es5 syntax
{% highlight c linenos %}
function printHelloEs5(){
  console.log('hello es5');
}
{% endhighlight %}

in es6 syntax
{% highlight c linenos %}
const printHelloEs6 = () => {
  console.log('hello es6');
}

printHelloEs5();
printHelloEs6();
{% endhighlight %}


Print multple values
{% highlight c linenos %}
console.log('hello' , 'bye');
console.warn(`this line ${'can make error'}`)
{% endhighlight %}


backtick can be used like template which is different to quote



%s for a String
%d for Number
{% highlight c linenos %}
console.log('name:%s', 'James');
console.log('age:%d', 31);
console.log('math:%d science:%d', 92, 84);
console.log('name:%s age:%d', 'James', 31);
{% endhighlight %}

{% highlight c linenos %}
const greeting1 = 'hello';
const greeting2 = 'bye';
const name1 = 'James';
const name2 = 'John';

const statement1 = `${greeting1} my name is ${name1}`;
const statement2 = `${greeting2}! my name is ${name1}`;

console.log('statement:', statement1);
console.log('statement:', statement2);
{% endhighlight %}
