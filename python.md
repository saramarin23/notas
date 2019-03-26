a print() function invoked with more than one argument outputs them all on one line;
the print() function puts a space between the outputted arguments on its own initiative.

The print() function separates its outputted arguments with spaces. This behavior can be changed, too.
The keyword argument that can do this is named sep (like separator). the sep argument's value may be an empty string, too.
<pre><code>print("My", "name", "is", "Monty", "Python.", sep="-")</pre></code>

list
----

<pre><code>numbers = [10, 5, 7, 2, 1]
print("List content:", numbers) # printing original list content

numbers[0] = 111
print("New list content: ", numbers) #current list content

numbers[1] = numbers[4] # copying value of the fifth element to the second
print("New list content:", numbers) # printing current list content</pre></code>

<b>the len() function</b>
The function takes the list's name as an argument, and returns the number of elements currently stored inside the list (in other words - the list's length).

<pre><code><b>del</b> numbers[1]
print(len(numbers))
print(numbers)</pre></code>

You can start a list's life by making it empty (this is done with an empty pair of square brackets) and then adding new elements to it as needed.

You may be familiar with adding individual data elements to a list by using the <code>.append()</code> method. However, if you want to combine a list with another array type (list, set, tuple), you can use the <code>.extend()</code> method on the list.

You can also use the <code>.index()</code> method to find the position of an item in a list. You can then use that position to remove the item with the <code>.pop()</code> method.

Functions
----
In general, functions come from at least three places:

  - from Python itself - numerous functions (like print()) are an integral part of Python, and are always available without any additional effort on behalf of the programmer; we call these functions built-in functions;
  - from Python's preinstalled modules - a lot of functions, very useful ones, but used significantly less often than built-in ones, are available in a number of modules installed together with Python; the use of these functions requires some additional steps from the programmer in order to make them fully accessible (we'll tell you about this in a while);
  - directly from your code - you can write your own functions, place them inside your code, and use them freely;

It's legal, and possible, to have a variable named the same as a function's parameter.
A situation like this activates a mechanism called shadowing:
  parameter x shadows any variable of the same name, but...
  ... only inside the function defining the parameter.
The parameter named number is a completely different entity from the variable named number.
