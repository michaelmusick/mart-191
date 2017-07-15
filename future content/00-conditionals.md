
From W3C.org Web Standards Course…
[https://www.w3.org/wiki/Programming\_-\_the\_real\_basics][1]

== Conditions ==
 
A condition is a test for something. Conditions are very important for programming, in several ways:
 
First of all conditions can be used to ensure that your program works, regardless of what data you throw at it for processing. If you blindly trust data, you’ll get into trouble and your programs will fail. If you test that the thing you want to do is possible and has all the required information in the right format, that won’t happen, and your program will be a lot more stable. Taking such precautions is also known as programming defensively.
 
The other thing conditions can do for you is allow for branching. You might have encountered branching diagrams before, for example when filling out a form. Basically, this refers to executing different “branches” (parts) of code, depending on if the condition is met or not.
 
The easiest condition is an \<code\>if\</code\> statement and its syntax is \<code\>if(condition){ do this … }\</code\>. The condition has to be true for the code inside the curly braces to be executed. You can for example test a string and set the value of another string dependent on its value:
 
\<pre\>&lt;script type="text/javascript"&gt;
var country = 'France';
var weather;
var food;
var currency;
if(country == 'England'){
  weather = 'horrible';
  food = 'filling';
  currency = 'pound sterling';
}
if(country == 'France'){
  weather = 'nice';
  food = 'stunning, but hardly ever vegetarian';
  currency = 'funny, small and colourful';
}
if(country == 'Germany'){
  weather = 'average';
  food = 'wurst thing ever';
  currency = 'funny, small and colourful';
}
var message = 'this is ' + country + ', the weather is ' + 
  weather + ', the food is ' + food + ' and the ' +
  'currency is ' + currency;
alert(message);
&lt;/script&gt;\</pre\>
 
Try it out yourself in my [http://dev.opera.com/articles/view/programming-the-real-basics/weather.html Weather if statement example](). Change the value of the country variable to see the different messages.
 
The conditional part is the country followed by the three equal signs. Three equal signs mean that the condition tests if the variable country has the value you test against but also the correct variable (data)type. You can test conditions with double equal signs, too, but that would mean that \<code\>if(x == 5)\</code\> would be true for x being 5 and x being “5”. Depending on what your program is doing, this could make quite a difference.
 
Other conditional test examples:
 
* x &gt; 0 - is x bigger than zero?
* x &lt; 0 - is x less than zero?
* x &lt;= 4 - is x less than or equal to four?
* x != 'hello' - is x not 'hello'?
* x - does x exist?
	 
Conditions can also be nested. Say for example you want to make sure that the country variable is set in the earlier example; you can do that this way:
 
\<pre\>&lt;script type="text/javascript"&gt;
var country = 'Germany';
var weather;
var food;
var currency;
if(country){
  if(country == 'England'){
weather = 'horrible';
food = 'filling';
currency = 'pound sterling';
  }
  if(country == 'France'){
weather = 'nice';
food = 'stunning, but hardly ever vegetarian';
currency = 'funny, small and colourful';
  }
  if(country == 'Germany'){
weather = 'average';
food = 'wurst thing ever';
currency = 'funny, small and colourful';
  }
  var message = 'this is ' + country + ', the weather is ' + 
weather + ', the food is ' + food + ' and the ' +
'currency is ' + currency;
  alert(message);
}
&lt;/script&gt;\</pre\>
 
Try it out yourself in my [http://dev.opera.com/articles/view/programming-the-real-basics/saferweather.html Safe-weather if statement example](). Change the value of the country variable to see the different messages.
 
Whereas the earlier example would always try to create the message regardless of country being available—and thus possibly throwing an error or stating “this is '''undefined''', the weather…” this version is more secure. If country is not defined the message will never be created.
 
Furthermore you can concatenate different conditions with “or” or “and” statements, to test whether either statement is true, or both are true, respectively. In JavaScript “or” is written as || and “and” is written as &amp;&amp;. Say you want to test if the value of x is between 10 and 20—you could do that with a condition stating \<code\>if(x &gt; 10 &amp;&amp; x &lt; 20)\</code\>. If you want to make sure that country is either “England” or “Germany” you use \<code\>if(country == 'England' || country == 'Germany')\</code\>.
 
There is also an \<code\>else\</code\> clause that will be applied every time the first condition isn’t true. This is very powerful if you want to react to any value, but single out one in particular for special treatment:

 
\<pre\>&lt;script type="text/javascript"&gt;
  var umbrellaMandatory;
  if(country == 'England'){
umbrellaMandatory = true;
  } else {
umbrellaMandatory = false;
  }
&lt;/script&gt;\</pre\>
 
Conditions are great, but they are a bit limited. What if you want to do something over and over again? Say your job is to add a paragraph tag around each of the values in an array? Using only conditions you’d need to hard-code cases for arrays of all the different lengths you'd be likely to come across:
 
\<pre\>&lt;script type="text/javascript"&gt;
  var names = new Array('Chris','Dion','Ben','Brendan');
  var all = names.length;
  if(all == 1){
names[0]() = '&lt;p&gt;' + names[0]() + '&lt;/p&gt;';
  }
  if(all == 2){
names[0]() = '&lt;p&gt;' + names[0]() + '&lt;/p&gt;';
names[1]() = '&lt;p&gt;' + names[1]() + '&lt;/p&gt;';
  }
  if(all == 3){
names[0]() = '&lt;p&gt;' + names[0]() + '&lt;/p&gt;';
names[1]() = '&lt;p&gt;' + names[1]() + '&lt;/p&gt;';
names[2]() = '&lt;p&gt;' + names[2]() + '&lt;/p&gt;';
  }
  if(all == 4){
names[0]() = '&lt;p&gt;' + names[0]() + '&lt;/p&gt;';
names[1]() = '&lt;p&gt;' + names[1]() + '&lt;/p&gt;';
names[2]() = '&lt;p&gt;' + names[2]() + '&lt;/p&gt;';
names[3]() = '&lt;p&gt;' + names[3]() + '&lt;/p&gt;';
  }
&lt;/script&gt;\</pre\>
 
This is just terrible and inflexible. Programming is meant to make our life easier and if you find yourself writing the same code over and over again, you are probably doing something wrong. Good programming means leaving the boring tasks to the machines and focusing on what you want to achieve.
 
In this case we need a '''loop''' instead of a condition, as we are doing exactly the same thing to each and every one of the items in the array, and the length doesn’t really matter. You’ll see the above example rewritten using a loop in the next section—compare the two, and see how much shorter the latter is!

[1]:	https://www.w3.org/wiki/Programming_-_the_real_basics
