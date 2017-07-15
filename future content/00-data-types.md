
From W3C.org Web Standards Course…
[https://www.w3.org/wiki/Programming\_-\_the\_real\_basics][1]

# Variable types
 
However, this would be boring as we can do all that with a simple calculator (after we typed 5318008, then turned it around and giggled, of course). Computers are more sophisticated and can make use of more complex variables. This is where variable types come in. Variables come in several types and different languages support different ones. The most common ones are:
 
* Float: a number, like \<code\>1.21323\</code\>, \<code\>4\</code\>, \<code\>100004\</code\> or \<code\>0.123\</code\>
* Integer: a natural number like \<code\>1\</code\>, \<code\>12\</code\>, \<code\>33\</code\>, \<code\>140\</code\> but not \<code\>1.233\</code\>
* String: a line of text like "\<code\>boat\</code\>", "\<code\>elephant\</code\>" or "\<code\>damn, you are tall!\</code\>"
* Boolean: either \<code\>true\</code\> or \<code\>false\</code\>, but nothing else
* Arrays: a collection of values like \<code\>1,2,3,4,'I am bored now'\</code\>
* Objects: a representation of an object. Objects are constructs that try to model instances of objects in the real world by having properties and methods. For example you could model a cat as an object and define that it has four legs, one tail and that it is ginger. You can also define that it has a way of purring by defining a \<code\>purr()\</code\> method and that it might demand a cheeseburger with a \<code\>getCheeseBurger()\</code\> method. You can also re-use the \<code\>cat\</code\> object and define another cat with all the properties of the original one but a grey colour.
	 
JavaScript is a “loosely typed” language, which means that you don't have to explicitly declare what type of data the variables are. You just need to use the \<code\>var\</code\> keyword to indicate that you are declaring a variable, and the browser will work out what data type you are using from the context, and use of quotes.
 
==== Floats and Integers ====
 
There is nothing magical or strange going on with these. You define variables and set their values to any number type.
 
\<pre\>&lt;script type="text/javascript"&gt;
  var fahrenheit = 123;
  var celsius = (fahrenheit - 32) * 5/9; 
  var clue = 0.123123;
&lt;/script&gt;\</pre\>
 
Floats and integers can be modified with any mathematical operators.
 
==== Booleans ====
 
Booleans are simple “yes or no” definitions. You assign them by using the \<code\>true\</code\> or \<code\>false\</code\> keywords.
 
\<pre\>&lt;script type="text/javascript"&gt;
  var doorClosed = true;
  var catCanLeave = false;
&lt;/script&gt;\</pre\>
 
==== Strings ====
 
Strings are lines of text that can contain any character. You define them in JavaScript by enclosing the text in single quotes or double quotes.
 
\<pre\>&lt;script type="text/javascript"&gt;
  var surname = 'Heilmann';
  var name = "Christian";
  var age = '33';
  var hair = 'Flickr famous';
&lt;/script&gt;\</pre\>
 
You can concatenate (a technical term that means “join together”) strings using the + operator but you cannot subtract strings from one another. For string modification you need to use functions the language provides you with. Simple concatenation on the other hand is as easy as this:
 
\<pre\>&lt;script type="text/javascript"&gt;
  var surname = 'Heilmann';
  var name = 'Christian';
  var age = '33';
  var hair = 'Flickr famous';
  var message = 'Hi, I am ' + name + ' ' + surname + '. ';
  message += 'I am ' + age + 'years old and my hair is ' + hair;
  alert(message);
 &lt;/script&gt;\</pre\>
 
Try out the [http://dev.opera.com/articles/view/programming-the-real-basics/flickrfamous.html string concatenation example]().
 
The += operator is a shortcut for "message = message +". The product of this script is the string “Hi I am Christian Heilmann. I am 33 years old and [http://flickr.com/photos/tags/thehairofchristianheilmann/ my hair is Flickr famous]()”.
 
There is a catch to remember when using concatenation versus adding values. If you want to add two values you need to make sure that both are numbers, not strings. The [http://dev.opera.com/articles/view/programming-the-real-basics/concatvsadd.html concatenation versus addition]() example shows the difference between the two. “5”+“3” is 53 and not 8! The easiest way to convert a string to a number is by prepending it with a "+", as shown in the example.
 
Most languages will not care if you use single or double quotes to enclose the string, as long as you don’t mix them. To stop the JavaScript interpreter from becoming confused about where the end of the string is, you need to comment out quotes contained in the string with a backslash:
 
\<pre\>&lt;script type="text/javascript"&gt;
  // this will cause an error, as the interpreter doesn't know 
  // what the things after the ' are. The string defined here is
  // 'Isn'.
  var stringWithError = 'Isn't it hard to get things right?';
  // This is not an error, all is fine
  var stringWithoutError = 'Isn\'t it hard to get things right?';
&lt;/script&gt;\</pre\>

==== Arrays ====
 
Arrays are very powerful constructs. An array is a collection of values, and each of the values can be a variable, or a real value. For example:
 
\<pre\>&lt;script type="text/javascript"&gt;
  var pets = new Array('Boomer','Polly','Mr.Frisky');
&lt;/script&gt;\</pre\>
 
You can access each of the values with the '''array''' counter, which is the index number in the array—think of it as being like looking up chapters in a book. The syntax is \<code\>arrayname[index]()\</code\>. So for example \<code\>pets[1]()\</code\> would give you the string “Polly”. But wait! I hear you ask—shouldn’t it be \<code\>pets[2]()\</code\> for Polly, given that it is the '''second''' value in the array? '''No'''—the counter is not 2, as computers start counting at 0, not at 1! This is a very common cause of confusion and errors.
 
Arrays automatically get a special information source for you: \<code\>length\</code\>. If you check the value of \<code\>pets.length\</code\> you will get 3 as there are 3 items in this array.
 
Arrays are great for describing collections of things that have something in common, and every language comes with dozens of handy functions to manipulate them—sorting, filtering, searching and so on.
 
==== Objects ====
 
If you have a collection of items that need more detailed descriptions than just a running number, then an Array won’t quite give what you need, and you’ll need to create an object. Objects are constructs in programming that represent or model real things, such a people, vehicles or tools.
 
Objects are a big and very clever and versatile part of programming and explaining them in detail here would be beyond the scope of this article. Let’s just say that an object is a thing that has several properties. Say for example you have a person object; you can define the different properties by appending them with a dot:
 
\<pre\>&lt;script type="text/javascript"&gt;
  var person = new Object();
  person.name = 'Chris';
  person.surname = 'Heilmann';
  person.age = 33;
  person.hair = 'Flickr famous';
&lt;/script&gt;\</pre\>
 
You can access the properties with dot notation (\<code\>person.age\</code\> would give you 33) or with the square bracket notation (\<code\>person['name']()
\</code\> gets you “Chris”). You will learn more about JavaScript objects later on in the course.
 
That is about the short and long of what value types variables can be. Another big part of programming is the structure and logic of your program. This is where two more programming ideas come into play: conditions and loops.

[1]:	https://www.w3.org/wiki/Programming_-_the_real_basics
