# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!
<p>
 Lists are collections of data of different types(Python) used mainly for storing. All elements in the list have a corresponding
index at which the element is present. Lists are mutable, meaning that even after their creation they can be altered in any way.
</p>

<p>
 Some methods for lists are:
<ul>
<li>
list.append() - used to add an element at the end of the list.
</li>
<li>
list.pop() - used to remove an element from a specific index or, by default, the last element
</li>
<li>
list.extend() - adds multiple values at once at the end of the list
</li>
<li>
list.sort() - sorts the list using Timsort.
</li>
</ul>	
</p>

#### What is the difference between a list/array and a set?
<p>
A set is collection of elements that is unordered and does not contain duplicates. A list, on the other hand, is ordered and can
contain duplicates 
</p>

#### What is the purpose and methods of a dictionary/map data structure?
<p>
A dictionary is the Python implementation of a hashtable. It contains keys each with an associated value. They are also dynamic and
mutable. The keys, however must of a non mutable type.
</p>
<p>
Some methods are
<ul>
<li>
dict.clear() - clears the dictionary
</li>
<li>
dict.get() - gets the value at a key, if the key does not exist it returns NOne
</li>
<li>
dict.items() - returns a list of key-value pairs in a dictionary.
</li>
</ul>
</p>

### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.
<p>

		def fibo(elements):
    			fib_list = []
    			fib_list.extend([0, 1])
    			count = 1
    			while count < elements-1:
        			fib_list.append(fib_list[count] + fib_lis[count- 1])
       				 count += 1
    			return fib_list

</p>

#### How do you find a max value in a list/array if you can’t use any built-in functions?
<p>
You assign to max the first value in the list. Then you iterate over the list from the second element onwards, 
if max is smaller than any of the elements you assign to max that value 
</p>

#### How do you find the average of values in a list/array if you can’t use any built-in functions?
<p>
You divide the sum of all elements in the list by the number of elements in the list.
</p>

#### What do we call an *in-place* sort?
<p>
An in-place sort is a sorting algorithm that does not use extra space to sort the list. It only modifies the order of the
elements. Examples are Selection Sort and Insertion Sort
</p>

#### Explain an algorithm which sorts a list!
<p>
Selection Sort
<ul>
<li>
Two loops are necessary to sort the list. One that starts from the begining and another that starts from the closest neighbour of the current element
</li>
<li>
<code>min_index</code> gets assigned to the index of the current element
</li>
<li>
If any element is smaller than the current one, its index is stored in the <code>min_index</code> variable
</li>
<li>
A swap between the current element and the element at the new <code>min_index</code> is made
</li>
</ul>
</p>

<p>

	def selection_sort(lst):
		for i in range(len(lst)):
        min_index = i
        for j in range(i + 1, len(lst)):
            if lst[min_index] > lst[j]:
                min_index = j
        lst[i], lst[min_index] = lst[min_index], lst[i]
    	return lst
				
</p>

### Programming paradigms - procedural

#### What is the call stack?
<p>
The call stack is a stack structure that stores information about the active subroutines of a program. 
</p>

#### What is “Stack overflow”?

<p>
When the stack reaches its maximum storage memory capacity, an error is thrown. It usually occurs when too much gets allocated to the stack. 

</p>

#### What are the main parts of a function?

<p>

	def add(a, b): --> Function title and the parameters
		s = a + b --> Function body and internal variables
		return s --> Return statement that returns the value and exists the function
</p>

### Programming languages - Python  
#### How do you use a dictionary in Python?

<p>
	You create an empty dictionary like this: <code>dict = {}</code>
</p>

<p>
	A dictionary is used to store key : data pairs.
</p>

#### What does it mean that an object is immutable in Python?

<p>
	Mutable objects can change their state or contents and immutable objects can’t change their state or content.
</p>

#### What is conditional expression in Python?

<p>
	A conditional statement is an if statement
</p>

#### What are different types of arguments in Python?
<p>
	There are three types of arguments in Python.
	<ul>
	<li>
	 	Default arguments --> are supplied to a function as default values. Whenever the function calls the function if he doesn't give a value for them they will have their default value
	</li>
	<li>
		Keyword arguments -->  the values passed through arguments are assigned to parameters in order, by their position
	</li>
	<li>
		Variable lenght arguments --> an asterisk (*) is placed before a parameter in function definition which can hold non-keyworded variable-length arguments and a double asterisk (**) is placed before a parameter in function which can hold keyworded variable-length arguments.
	</li>
	</ul>
</p>

#### What is variable shadowing? (context: variable scope)

<p>
	Refers to a variable declared in an inner scope that has the same name as a variable declared in an outer scope.
</p>

#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?

<p>
	Index error when removing, nothing when adding.
</p>

#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
<p>
	When referring a name in our code the search is carried on through the following four scopes: local, enclosing, global and built-in. LEGB stands for Local, Enclosing, Global and Built-in.
</p>

#### If you need to access the iterator variable after a for loop, how would you do it in Python?

<p>
	print(i)
</p>

#### What type of elements can a list contain in Python?

<p>
 int, float, list, string, dictionary, tuple
</p>

#### What is slice operator in Python and how to use?

<p>
 It is used to extract a part from the string or list.

	a = 'abcdse'
	b = a[2:-1:2] starting_point, ending_point, step
	b  = 'cs'

</p>

#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
<p>
<ul>
<li>
 <b>+</b> --> only if used with another list, will combine the two lists
</li>
<li>
<b>*</b> --> used with an int, will multiply the list that many times and create a new list
</li>
<li>
<b>-</b>  --> can't be used
</li>
<li>
<b>/</b> --> doesn't work
</li>
</ul>
</p>

#### What is the purpose of the in and not in membership operators in Python?

<p>
	It checks if a value is present in a collection.
</p>

#### What does the + operator mean when used with strings in Python?

<p>
	It concatenates the two strings.
</p>

#### Explain f strings in Python?
<p>
	F-strings provide a way to embed expressions inside string literals, using a minimal syntax. It should be noted that an f-string is really an expression evaluated at run time, not a constant value. In Python source code, an f-string is a literal string, prefixed with f, which contains expressions inside braces. The expressions are replaced with their values.
</p>

#### Name 4 iterable types in Python!
<p>
	<ul>
	<li> list
	</li>
	<li> tuple
	</li>
	<li> string
	</li>
	<li> range
	</li>
	</ul>
</p>

#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?\

<p>
	A comprehension executes immediately and returns a list, whereas a generator returns an object that can be iterated. The generator items can't be acessed by index. Also the generator is considered a lazy iterator, meaning that it does not store values in the memory.
</p>


#### Does the order of the function definitions matter in Python? Why?
<p>
	The order does not matter because python is a dynamically typed language, meaning that it stores the function at some memory location and holds it there until a call is made
</p>

#### What does unpacking mean in Python?

<p>
	Can be used to divide a list or a dictionary in multiple variables.
</p>

#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?

<p>
	The variable will have the value <code>None</code>
</p>

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
<ul>
<li>
 logging
</li>
<li>
 conditional breakpoints
</li>
<li>
	printing
</li>
</ul>

#### What does step over, step into and step out mean while using the debugger?

<ul>

<li>
	step over --> If the line contains a function the execution will return only the result and the debugger will not debug the function line by line.
</li>
<li>
	step into --> If the line contains a function, the debugger will go inside it and debug every line.
</li>
<li>
	step out -->  It returns to the line where the current function was called
</li>

</ul>

#### How can you start to debug a program from a certain line using the debugger?

<p>
	 Using a breakpoint.
</p>

### Version control

#### What are the advantages of using a version control system?
<p>
	You can access previous versions, multiple people can collaborate in an easy manner, in case something goes bad you can also revert
</p>

#### What is the difference between the working directory, the staging area and the repository in git?
<ul>
	<li>
		The working directory is the directory in which the files you are working on are stored.
	</li>
	<li>
		The staging area is a space where changes to files are kept until they are either pushed or checked out.
	</li>
	<li>
		The repository is a copy of the entire project stored somewhere.
	</li>
</ul>

#### What are remote repositories in git?
<p>
	 Remote repositories are copies of the original repoository stored on ones computer.
</p>

#### Why does a merge conflict occur?
<p>
	When two or more users edit the same file, or when something that is pulled changes something that has benn changed locally.
</p>

#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
<p>

		git add .
		git commit -m "Message"
		git push origin branch
</p>

#### What does it mean atomic commits and descriptive commit messages?
<p>
	An atomic commit revolves around a commit that changes a single thing. Descriptive commit messages are messages the convey what the commit message is about in a compact form.
</p>

#### What’s the difference between git and GitHub?
<p>
	git is a software whereas GitHub is an online platform used to store your repos.
</p>


## Software design

### Clean code

#### What does clean code mean?
<p>
	It is code that is easy to read and to maintain and follows the adopted design principles
</p>

#### What steps do we usually do during a clean code refactoring?
<ul>
<li>
	Formating
</li>
<li>
	Variable rename
</li>
<li>
	Cleaning duplicate code
</li>

<li>
	Dividing large blocks of code into methods.
</li>
</ul>

### Error handling

#### What is exception handling?

<p>
	Exception handling refeers to the way an exception is processed in order to make sure it does not hinder the execution of a program.
</p>

#### What are the basics of exception handling in Python?
<p>
	A <code>try except</code> block that firs catches the error and then provides code to handle it.
</p>

#### In which case should we catch an exception? Why?
<p>
	An exception should be handled especially when it leads to an unexpected end of the program. Doing so will ensure that the program will continue to run.
</p>

#### What can/should we do with an exception in the ‘except’ block?

<p>
	We should write code that will handle the exception in an ellegant manner.
</p>

#### What does the else and finally statement do in a try-except block in Python?

<p>
	The finally statement executes wether or not the try statement produces an exception. Else will be executed only if the try block does not generate an exception.
</p>

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

<p>
	To discuss what went well, what went wrong, and what areas could be improved.
</p>

## Programming environment

### Unix

#### What is UNIX and what is Linux?
<p>
	Linux is a kernel but also denotes the family of operating systems which are based on this kernerl. On the other hand UNIX is a full blown operating system developed by AT&T in the 70's.
</p>

#### What do we call the shell in Linux?
<p>
	The shell used in Ubuntu is called BASH (Bourne Again Shell) 
</p>

#### What does root mean in a Linux environment?
<p>
	root is a particular user account that has access to all commands, files and folders on the system.
</p>

#### How do you access your personal files in Linux?
<p>
	<code> cd ~</code> navigates to your home folder.
</p>

#### How can you install an application in Linux?
<p>
	Either visually from a software center or via terminal.
</p>

#### What is package management in Linux, what are repositories?
<p>
	Packet management is a way to mantain software on your computer. Repositories are storage locations from which the system receives software and updates.
</p>

#### How do you navigate in the filesystem with the command line?

<p>
	with the <code> cd </code> command
</p>

#### What does the following commands do: mkdir, rm, cat, cp, touch?
<ul>
<li>
	<code>mkdir</code> creates a new folder
</li>
<li>
	<code>rm</code> deletes a file
</li>
<li>
	<code>cat</code> reads data from files and outputs it, it stands for catenate
</li>
<li>
	<code>cp</code> copies a file
</li>
<li>
	<code>touch</code> creates a new file
</li>
</ul>

#### How can you look up what does a command do in Linux if you have no internet connection?
<p>
	<code>man {command_name}</code>
</p>

#### What does the following commands do: head, tail, more, less?\
<ul>
<li>
	<code> head </code> displays only the first 10 lines of a file
</li>
<li>
	<code> tail </code> displays only the last 10 lines of a file
</li>
<li>
	<code> more </code> displays the text in a file in a scrollable format
</li>
<li>
	<code> less </code> displays contents of a file one screen at a time.
</li>
</ul>

#### How do you download a file from internet using the terminal?

<p>
	Using <code>curl</code> or <code>curl</code> commands.
</p>
