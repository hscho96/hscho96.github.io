---
layout: post
title:  "Nodejs - Printing Values using console.log"
date:   2020-06-19 22:47:13 +0800
categories: Nodejs
tags: Javascript Nodejs
---

"console.log" shows the result of the program. In short, it leaves logs for debugging.


You can run the program using "Ctrl + Shift + B" (In my case, I'm using Atom),  
I had to download package which is called "script" to run and see the result of the code.  
- https://github.com/rgbkrk/atom-script

It is really easy to print out hello  
{% highlight ruby %}
console.log('hello');
print_hi('Tom')
{% endhighlight %}


in es5 syntax
{% highlight ruby %}
function printHelloEs5(){
  console.log('hello es5');
}
{% endhighlight %}

in es6 syntax
{% highlight ruby %}
const printHelloEs6 = () => {
  console.log('hello es6');
}

printHelloEs5();
printHelloEs6();
{% endhighlight %}  





It is also easy to print multple values by using comma and quotes.
{% highlight ruby %}
console.log('hello' , 'bye');
console.warn(`this line ${'can make error'}`)
{% endhighlight %}


Backtick can be used like template which is different to quote  
("%s" for a String)  
("%d" for Number)
{% highlight ruby %}
console.log('name:%s', 'James');
console.log('age:%d', 31);
console.log('math:%d science:%d', 92, 84);
console.log('name:%s age:%d', 'James', 31);
{% endhighlight %}


However, using "%s" and "$d" for many variables won't be simple and clear to see.  
Therefore, declaring variables would facilitate managing various variables.  
In this case, we have to distinguish "backtick" and "quote" since they look similar.
{% highlight ruby %}
const greeting1 = 'hello';
const greeting2 = 'bye';
const name1 = 'James';
const name2 = 'John';

const statement1 = `${greeting1} my name is ${name1}`;
const statement2 = `${greeting2}! my name is ${name1}`;

console.log('statement:', statement1);
console.log('statement:', statement2);
{% endhighlight %}
