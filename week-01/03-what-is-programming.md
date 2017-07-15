
# What is Programing? 

> Order, I will have order!

Programming in the most basic form is issuing commands and seeing that they get executed. It is a mixture of math and linguistics: you define a lot of calculations and you need to tell machines to solve them by giving orders using the right grammar. Grammar in programming is syntax and differs a lot from language to language.
For example, the following two code snippets fulfill the same task, but the former is JavaScript and the latter is PHP:
var fahrenheit = prompt('Enter temperature in Fahrenheit',0);
var celsius = (fahrenheit - 32) * 5 / 9;
alert(celsius);

$fahrenheit = $_GET['fahrenheit']();
$celsius = ($fahrenheit - 32) * 5 / 9;
echo $celsius;
Try out the JavaScript farenheit to celsius conversion example.
Programming languages are interpreted to be turned into actions or results. Some languages, such as JavaScript are interpreted by a web browser and all you need to do to make them “do stuff” is put them inside an HTML document and open this in a browser. Other programming languages need to be translated (compiled) in an extra step to become executable. Deep down, all computers only understand zeros and ones, but above that there are multiple levels of languages, each fulfilling different tasks.



# References
Some of the material above was taken from W3C.org course on Web Standards. Specifically, material was taken from [<cite>Programming - the real basics!</cite>, written by Christian Heilmann][2]

[2]:	https://www.w3.org/wiki/Programming_-_the_real_basics