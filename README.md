# CS50-Python-Harvard

Functions and Variables

1. Function
  
   print("...")
   // python3 hello.py
   
   input("...?")
   //会有自动输入区域
   // string
   
   print("hello, " + name)
   print("hello,", name) 
   // comma is for multiple arguments, but it has extra space
   
2. Argument

    what you want in input/print

3. Side Effects

    appearance = 呈现状态，比如print出来的东西

4. Variables 变量，可以变化的
  
    name = input（"What's your name? ")
    单等于号：有assign的作用，代表assign right to the left
    
5. Comments

    # explanation with no meaning; 
    # structure;
    
    Or 
    
    """
    here, here
    """
    
6. Pseudocode

    outline/structure the design, may only include comments. Add the code later on.
    
7. Name the Parameters

   tell you what you can pass in the funtion
   what the input are called -- parameters
   
   use the fucntion and pass in values inside of those parentheses -- arguments
    
    eg:
    print(*objects, sep=' ', end='\n', )
    sep: separator - multiple arguments will have a new space
    \n: new line, 所以会自动换行。为了取消，可以手写
    
    print("hello, ", end="")
    print(name)
    // 这样的话，名字不会空行了，因为去除了 \n
    
    print("hello, ", name, sep="???")
    $ hello, ???Dvaid
    
    '' 或者 "" 都可以，但是要一致。
    
8. 如何在引号里面用引号？
  
    print("hello, "friend"")
    $ SyntaxError
    
    print(‘hello, "friend"’)
    $ hello, "friend"
    // 用不同的引号，用于区别
    
    print("hello, \"friend\"")
    $ hello, "friend"
    // backslash: \
    // 让电脑知道里面是引用
    
    
9. f-string; format string

    name = input("What's your name? ")
    print(f"hello, {name}")
    $ python hello.py
    What's your name? David
    hello, David
    // f是在告诉电脑这是format的string
    // 只是告诉另一种表达

10. String Methods

    有时候客户的输入不标准,需要对于输入做出改变。之前讲了输入一般是string，所以一般处理的是string
    见跟多操作: https://docs.python.org/3/library/stdtypes.html#string-methods
    
    # Ask user for their name
    name = input("What's your name? ")
    
    # Remove whitespace from str
    name = name.strip()
    
    # Capitalize user's name
    name = name.title()
    //name = name.capitalize()
    // capitalize the first letter (David malan)
    // so we decide to use .title()
    
    # Say hello to user
    print(f"hello, {name}")
    
    $ python hello.py
    What's your name?      david malan
    hello, David Malan
    
    
    把冗长的代码简化：
    # Ask user for their name
    name = input("What's your name? ")
    
    # Remove whitespace from str and capitalize user's name
    name = name.strip().title
    
    # Say hello to user
    print(f"hello, {name}")
    
    超级简化：
    # Ask user for their name 
    name = input("What's your name? ").strip().title
    
    # Say hello to user
    print(f"hello, {name}")

11.

12.

13.

14.
