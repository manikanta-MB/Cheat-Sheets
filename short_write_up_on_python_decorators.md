# Python Decorators
The main Objective of “Decorators” is to extend the capability or functionality of an existing function without touching that function.<br />
Following are some examples on how to use Decorators,
### Example 1
```python3
def divide(a,b):
    return a//b
```
Above function can return the floor division of two arguments, but what if the second argument is zero?.<br />
In that case , it will return ZeroDivisionError.So now, you will change that function by adding some conditions.<br />
But Can you do this without touching that function?<br /><br />
**Yes** , you can do it using “Python Decorators”. See the Code below,
### Example 2
```python3
def divide_by_zero_check(func):
    def inner(a,b):
        if(b==0):
            return “You can’t divide a number by zero”
        else:
            return func(a,b)
    return inner

@divide_by_zero_check
def divide(a,b):
    return a//b
```
If you call the **divide(3,0)**, first call will be taken by **divide_by_zero_check** decorator,<br />
and then it will check if the second argument is zero, if yes, it will simply return some string,<br/>
else will call the original **divide** function with the same arguments.<br /><br />
If you want to observe the flow of the decorators, just observe the below statements.<br />
Following are flow statements for the above decoratos,
```
divide                             ---->      func (in divide_by_zero_check)
inner (in  divide_by_zero_check)   ---->      divide
```
First **divide** function definition will be stored in **func** variable,<br />
And then **inner** function defintion will be stored in **divide** variable.<br /><br />
When you call **divide(3,0)** , because **inner** function definition is in **divide** variable, first **inner** function will be called with these arguments.<br />
In the **inner** function, when we call **func(a,b)** in else condition, **divide(a,b)** will be called becaue **divide** function definition is stored in **func** variable.
<br /><br />

We can use Multiple Decorators for one function.<br />
All these decorators form a Decorator Chaining.<br />
Following is an example of using Multiple Decorators,
### Example 3
```python3
def decor1(func):
    def inner():
        print(“Decorator 1)
        func()
    return inner

def decor2(func):
    def inner():
        print(“Decorator 2)
        func()
    return inner

@decor1
@decor2
def wish():
    print(“Good Morning”)
```
when we call wish() function, then output will be in the following order,
```
Decorator 1
Decorator 2
Good Morning
```
Following are flow statments for above decorators,
```
wish                ---->     func (in decor2)
inner (in decor2)    ---->    func (in decor1)
inner (in decor1)    ---->    wish
```
THAT’S IT.<br />
These are the basic things about Python Decorators.<br />
If you could understand the above statements, you can easily get into the advanced material.
