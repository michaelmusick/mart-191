
From W3C.org Web Standards Course…
[https://www.w3.org/wiki/Programming\_-\_the\_real\_basics][1]

# Variables
 
The first step towards understanding programming is looking back at algebra. If you remember from school, algebra starts with writing terms such as the following.
 
\<pre\>3 + 5 = 8\</pre\>
 
You start performing calculations when you introduce an unknown, for example x below:
 
\<pre\>3 + x = 8\</pre\>
 
Shifting those around you can determine x:
 
\<pre\>x = 8 - 3 
-&gt; x = 5\</pre\>
 
When you introduce more then one you make your term more flexible - you are using variables:
 
\<pre\>x + y = 8\</pre\>
 
You can change the values of x and y and the formula can still be true:
 
\<pre\>x = 4
y = 4\</pre\>
 
or
 
\<pre\>x = 3
y = 5\</pre\>
 
The same works with programming languages—in programming, variables are containers for values that can vary. Variables can hold all kind of values and also the results of calculations. Variables have a name and a value separated by an equals sign (=). Variable names can be any letter or word, but bear in mind that there are restrictions from language to language of what you can use, as some words are reserved for other functionality.

To keep things easy, let’s use JavaScript as an example programming language in this article (logical, since this section of the web standards curriculum is all about JavaScript programming!) The following defines two variables, calculates the result of adding the two and defines this result as a value of a third variable.
 
Note: The \<code\>&lt;script&gt;\</code\> tags are there to tell the browser that the text inside is a scripting language and that it should be interpreted as such. The \<code\>"text/javascript"\</code\> type attribute tells the browser what language it is.

\<pre\>&lt;script type="text/javascript"&gt;
var x = 5;
var y = 6;
var result = x + y;
&lt;/script&gt;\</pre\>
 
The interpreter goes through the code instruction by instruction, with each instruction ending in a semicolon. The semicolon notifies the interpreter of the end of an instruction, much like a full stop or an exclamation mark defines the end of a sentence in human languages.
 
In English, this construct would be as follows:
 
* Here comes something that is not HTML; bring forth a translator that understands a language of the type JavaScript that is text based.
* Define a new variable (that is the \<code\>var\</code\> keyword) called x and assign it the value 5. End of instruction.
* Define a new variable called y and assign it the value 6. End of instruction.
* Define a new variable called result and assign it the result of adding x and y as its value. End of statement. (As there is a calculation in the assignment of the variable result the interpreter then checks the value of x, checks the value of y, adds the two and sets the value of result to the outcome—11).
* Enough of this strange language—go back to HTML and tell the translator to leave again.
	 
You can do all kind of calculations with variables by adding operators in between them. There are the classics like adding with a plus sign operator and subtracting with a minus sign operator. For multiplication you have to use an asterisk (*) and for dividing, a slash (/). The following example shows some calculations that are possible. Notice the texts preceded by a double slash //—these are JavaScript comments. When a JavaScript interpreter encounters these in a script it will not try to execute what follows on that line, and skips it—these are comments made for humans and not to be interpreted by the browser.
 
\<pre\>&lt;script type="text/javascript"&gt;
var x = 5;
var y = 6;
var z = 20;
var multiply = x * y * z;
// multiply will be 600 
var divide = x / y;
// divide will be 0.8333333333333334
var addAndDivide = (x + z) / y;
// addAndDivide = 4.166666666666667
var half = (y + z) / 2;
// half will be 13
&lt;/script&gt;\</pre\>
 
As you can see you can mix and match any variable, and also use variables along with fixed values in calculations; you can also group them with parenthesis to override the natural order of operators (parentheses first, then multiplication or dividing, then adding or subtracting and all those Math lesson classics).
 

[1]:	https://www.w3.org/wiki/Programming_-_the_real_basics