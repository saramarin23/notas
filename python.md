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


Note: None is a keyword.

There are only two kinds of circumstances when None can be safely used:

when you assign it to a variable (or return it as a function's result)
when you compare it with a variable to diagnose its internal state.
Just like here:

<pre><code>value = None
if value == None:
   print("Sorry, you don't carry any value")</pre></code>

Don't forget this: if a function doesn't return a certain value using a return expression clause, it is assumed that it implicitly returns None.

1. A variable that exists outside a function has a scope inside the function body (Example 1) unless the function defines a variable of the same name (Example 2, and Example 3), e.g.:

Example 1:

<pre><code>var = 2

def multByVar(x):
    return x * var

print(multByVar(7))    # outputs: 14</pre></code>

Example 2:

<pre><code>def mult(x):
    var = 5
    return x * var

print(mult(7))    # outputs: 35</pre></code>

Example 3:

<pre><code>def multip(x):
    var = 7
    return x * var

var = 3
print(multip(7))    # outputs: 49</pre></code>

2. A variable that exists inside a function has a scope inside the function body (Example 4), e.g.:

Example 4:

<pre><code>def sum(x):
    var = 7
    return x + var

print(sum(4))    # outputs: 11

print(var)    # NameError</pre></code>

3. You can use the global keyword followed by a variable name to make the variable's scope global, e.g.:

<pre><code>var = 2
print(var)    # outputs: 2

def retVar():
    global var
    var = 5
    return var

print(retVar())    # outputs: 5

print(var)    # outputs: 5</pre></code>

dictionaries
-----

Assigning a new value to an existing key is simple - as dictionaries are fully mutable, there are no obstacles to modifying them. Esto sirve también para añadir una no existente:

<pre><code>dict = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

dict['cat'] = 'minou'
print(dict)</pre></code>

Adding a new key-value pair to a dictionary is as simple as changing a value - you only have to assign a value to a new, previously non-existent key.

Note: this is very different behavior compared to lists, which don't allow you to assign values to non-existing indices.

Let's add a new pair of words to the dictionary - a bit weird, but still valid. (Hay otra manera de añadir):

<pre><code>dict = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

dict.update({"duck" : "canard"})
print(dict)</pre></code>

Note: removing a key will always cause the removal of the associated value. Values cannot exist without their keys.

<code>del dict['dog']</code>

To remove the last item in a dictionary, you can use the <code>popitem()</code> method:

<pre><code>dict = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

dict.popitem()
print(dict)    # outputs: {'cat' : 'chat', 'dog' : 'chien'}</pre></code>
