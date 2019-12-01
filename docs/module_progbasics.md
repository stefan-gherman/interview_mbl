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
#### What is “Stack overflow”?
#### What are the main parts of a function?

### Programming languages - Python  
#### How do you use a dictionary in Python?
#### What does it mean that an object is immutable in Python?
#### What is conditional expression in Python?
#### What are different types of arguments in Python?
#### What is variable shadowing? (context: variable scope)
#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
#### What type of elements can a list contain in Python?
#### What is slice operator in Python and how to use?
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
#### What is the purpose of the in and not in membership operators in Python?
#### What does the + operator mean when used with strings in Python?
#### Explain f strings in Python?
#### Name 4 iterable types in Python!
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
#### Does the order of the function definitions matter in Python? Why?
#### What does unpacking mean in Python?
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
#### What does step over, step into and step out mean while using the debugger?
#### How can you start to debug a program from a certain line using the debugger?

### Version control

#### What are the advantages of using a version control system?
#### What is the difference between the working directory, the staging area and the repository in git?
#### What are remote repositories in git?
#### Why does a merge conflict occur?
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
#### What does it mean atomic commits and descriptive commit messages?
#### What’s the difference between git and GitHub?

## Software design

### Clean code

#### What does clean code mean?
#### What steps do we usually do during a clean code refactoring?

### Error handling

#### What is exception handling?
#### What are the basics of exception handling in Python?
#### In which case should we catch an exception? Why?
#### What can/should we do with an exception in the ‘except’ block?
#### What does the else and finally statement do in a try-except block in Python?

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

## Programming environment

### Unix

#### What is UNIX and what is Linux?
#### What do we call the shell in Linux?
#### What does root means in a Linux environment?
#### How do you access your personal files in Linux?
#### How can you install an application in Linux?
#### What is package management in Linux, what are repositories?
#### How do you navigate in the filesystem with the command line?
#### What does the following commands do: mkdir, rm, cat, cp, touch?
#### How can you look up what does a command do in Linux if you have no internet connection?
#### What does the following commands do: head, tail, more, less?
#### How do you download a file from internet using the terminal?
