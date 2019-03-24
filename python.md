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