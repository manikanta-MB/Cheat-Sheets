# How to Write Performant Code in Python
Using Python, you can quickly create a program that solves a business problem or fills a practical need.<br />
However, the solutions you reach when developing quickly aren’t always optimized for python performance.<br /><br />
Following are some of the tips that you can follow to write perfomant code in python,
### 1. Use List Comprehensions instead of Loops
While Creating the Lists, use List Comprehensions instead of writing loops and extending the lists in that loop.
List comprehensions are faster than loops. You can’t find the difference when you run with small amount of data,
but you will get the use of it while dealing with medium to large amount of data.
### 2. Remember using built-in functions
Python comes with a lot of inbuilt libraries. We can write Highly efficient and and quality, but it is hard to beat Python Standard Libraries,
because they are highly optimized. So always try to use builit in functions whenever it is possible.
### 3. Consider writing your own generator
Using generators is always better when we deal with the large amount of data.
Instead of first storing all the items and processing each item in a for loop, we can use the generators to get each item on demand and process that item.
Generators are extremely faster.
### 4. Use “in” Keyword
when you search for an item in a list, always consider using “in” keyword. Python has it’s optimized way to search for something in a list while using “in” keyword in Code.
### 5. Be Lazy with your Module importing
Instead of importing all your modules at the start of program, try to load each one when you need them. Becaues loading all the modules at startup may somewhat slowdown your program. 
  So when you load them only when you need them, it will help in distributing the loading time of modules more evenly, which may reduce peaks of memory usage.
### 6. Use sets and Unions
Always try to use sets and corresponding methods instead of using for loops whenever it is possible. Because sets and corresponding built-in functions are much faster than loops.
### 7. Remember to use multiple assignment
when you need to assign multiple variables, always consider using multiple assignment statements because they are cleaner and faster.
### 8. Avoid global variables
Python is faster in retrieving local variables than global one. So avoid that global keyword as much as you can.
### 9. Use join() to concatenate strings
To concatenate multiple strings, always consider using “join()” method instead of using “+” operator. Because when you use “+” operator, for every concatenation of two strings, 
  it will create a new string and then copy that entire string for the next concatenation. “join()” method provides much faster and memory efficient implementation.
### 10. Keep up-to-date on latest python releases
Python maintainers passionate about continually making the language faster and more robust. Each new release of python improves the performance and security of python. 
  So be sure that libraries you want to use are compatible with the newest version.
### 11. Use “while 1” for an infinite loop
Instead of using “while True” , try to use “while 1” for an infinite loop. This is a single jump operation, as it is a numerical comparision. It improves the performance.
### 12. Learn itertools
Try to learn the functions which are available in “itertools” module. Because there are so many useful functions available and also they provide a lot more memory efficient and faster implementations.
### 13. Try decorator caching
While using the caching in recursive programs, try to use python inbuilt caching decorators like the one “lru_cache” method provided by functools module. Because it is a very quick way to implement and also improves performance.
### 14. Use keys for sorts
when you need to sort the nested lists, instead of using your own sorting methods, always consider to use built-in “sort” method of list as well as “key” argument in that sort method. 
  By using “key” argument, we can easily sort the nested lists just by specifying index of the item on which we want to sort. This is much quicker way to to implement and also it improves performance because of inbuilt “sort” method. 
  Python provides much more optimized implementations when we use this “sort” method.
