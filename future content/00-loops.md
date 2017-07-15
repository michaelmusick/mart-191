
From W3C.org Web Standards Course…
[https://www.w3.org/wiki/Programming\_-\_the\_real\_basics][1]

== Loops ==
 
Loops are repetitive conditions where one variable in the loop changes. The easiest form of a loop is the \<code\>for\</code\> statement. This one has a syntax that is similar to an \<code\>if\</code\> statement, but with more options:
 
\<pre\>for(condition;end condition;change){
  // do it, do it now
}\</pre\>
 
Normally what you do with a \<code\>for\</code\> loop is to execute the code in the curly braces several times. For this you need to define an iterator variable and keep changing it during the loop until the variable value meets the end condition (which causes the interpreter to exit the loop and carry on to the next part of the code). For example:
 
\<pre\>&lt;script type="text/javascript" charset="utf-8"&gt;
  for(var i = 0;i &lt; 11;i = i + 1){
// do it, do it now
  }
&lt;/script&gt;\</pre\>
 
Here we define a variable \<code\>i\</code\> as having an initial value of 0 and then do a check to see if it has reached 11 yet (is it smaller than 11?). The change equation—\<code\>i = i + 1\</code\>—adds one to \<code\>i\</code\> every time the loop executes and goes through another iteration. This means that this loop executes 11 times. If you add two to \<code\>i\</code\> on every iteration it executes only 6 times:
 
\<pre\>&lt;script type="text/javascript"&gt;
  for(var i = 0;i &lt; 11;i = i + 2){
// do it, do it now
  }
&lt;/script&gt;\</pre\>
 
Using a loop the paragraph adding example we saw above gets a lot shorter and simpler:
 
\<pre\>&lt;script type="text/javascript"&gt;
  var names = new Array('Chris','Dion','Ben','Brendan');
  var all = names.length;
  for(var i=0;i&lt;all;i=i+1){
names[i]() = '&lt;p&gt;' + names[i]() + '&lt;/p&gt;';
  }
&lt;/script&gt;\</pre\>
 
Notice that you can use the value of \<code\>i\</code\> as the array counter inside the loop. This is the power of loops—not only can you do the same thing over and over again; you also know in every iteration how many times you have already done it.

[1]:	https://www.w3.org/wiki/Programming_-_the_real_basics
