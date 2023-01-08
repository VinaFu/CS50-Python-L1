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

    用#来表示explanation with no meaning; structure;
    
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
  
  10.1
  
    #Ask user for their name
    name = input("What's your name? ")
    
    #Remove whitespace from str
    name = name.strip()
    
    #Capitalize user's name
    name = name.title()
    //name = name.capitalize()
    // capitalize the first letter (David malan)
    // so we decide to use .title()
    
    #Say hello to user
    print(f"hello, {name}")
    
    =============
    $ python hello.py
    What's your name?      david malan
    hello, David Malan
    
    
  10.2 把冗长的代码简化：
  
    #Ask user for their name
    name = input("What's your name? ")
    
    #Remove whitespace from str and capitalize user's name
    name = name.strip().title
    
    #Say hello to user
    print(f"hello, {name}")
    
    超级简化：
    #Ask user for their name 
    name = input("What's your name? ").strip().title
    
    #Say hello to user
    print(f"hello, {name}")
    
  10.3 split
  
    #Ask user for their name 
    name = input("What's your name? ").strip().title
    
    #Split user's name into first name and last name
    first, last = name.split(" ")
    // 暗示用空格隔开的，前面是first，后面是last
    // 下面引用，引的first这个variable
    
    #Say hello to user
    print(f"hello, {first}")
    
    =============
    $ python hello.py
    What's your name? david malan
    hello, David

11. int - whole number, no decimals

    +, -, *, /, %(modulo- reminder), //(除数)
  
  11.1 create a calculator
  
    code calculator.py (- terminal; - build a new python file)
    
    x = input("What's x? )
    y = input("What's y? )
    
    z = x + y
    print(z)
    
    $ python calculator.py
    What's x? 1
    What's y? 2
    12
    //bug: it comcatenates, but input=string, + in string means concatenatination
    
    x = input("What's x? )
    y = input("What's y? )
    
    z = int(x) + int(y)
    print(z)
    
    $ python calculator.py
    What's x? 1
    What's y? 2
    3
    
  11.2 Nest function
    
    x =int(input("What's x? ))
    y =int(input("What's y? ))
   
    print(x + y)
    
    $ python calculator.py
    What's x? 1
    What's y? 2
    3
    // 因为z只用了一次，没必要特地设置新的variable

12. Interactive mode: 可以直接看结果，互交模式

    directly type in the terminal:
    $ python
    >>> (which means interactive mode)
    eg:
    >>> 1+1
    2
    >>>print("hello, world")
    hello, world

13. Float - with decimals（Round）

  13.1
  
    x =float(input("What's x? ))
    y =float(input("What's y? ))
   
    print(x + y)
    
    $ python calculator.py
    What's x? 1.2
    What's y? 3.4
    4.6
    
    but if you want to round the answer
    round(number[, ndigits])
    // [] optional，可有可无
    // 表示你想近似到哪里；默认是整数
    
    x = float(input("What's x? ))
    y = float(input("What's y? ))
   
    z = round(x + y)
    print(z)
    
    $ python calculator.py
    What's x? 1.2
    What's y? 3.4
    5
    
  13.2 面对大的数值,想要分隔符
  
    x = float(input("What's x? ))
    y = float(input("What's y? ))
   
    z = round(x + y)
    
    print(f"{z:,}")
    // :表示分隔
    
    $ python calculator.py
    What's x? 999
    What's y? 1
    1,000
  
  13.3 Division
  
    x = float(input("What's x? ))
    y = float(input("What's y? ))
   
    z = x / y
    
    print(z)
    
    $ python calculator.py
    What's x? 2
    What's y? 3
    0.6666...(limited digits)
    
    For infinte or long digits, round it to precise digits
    
    x = float(input("What's x? ))
    y = float(input("What's y? ))
   
    z = round(x / y, 2)
    
    print(z)
    
    $ python calculator.py
    What's x? 2
    What's y? 3
    0.67
    
  另一种相同的方法，用format 方法
    
    x = float(input("What's x? ))
    y = float(input("What's y? ))
   
    z = x / y
    
    print(f"{z:.2f}")
    
    $ python calculator.py
    What's x? 2
    What's y? 3
    0.67

14. def - define a function yourself

  14.1
  
    def hello():
        print("hello")
    
    name = input("What's your name? ")
    hello(name)
    =============
    $ python hello.py
    What's your name? David
    hello
    David
    
  14.2 more customerize - one line + default
  
    def hello(to):
        print("hello,", to )
        // "to" refers to objects here, what you put inside
    
    name = input("What's your name? ")
    hello(name)
    
    =============
    $ python hello.py
    What's your name? David
    hello, David
    
    
    def hello(to="world"):
        //默认object是world，有新值，则新值替换
        print("hello,", to )
    
    hello()
    name = input("What's your name? ")
    hello(name)
    
    =============
    $ python hello.py
    hello, world
    What's your name? David
    hello, David
    
  14.3 结构顺序 + call
  
    **** Tips:
    一般把自己的function写在运用它之前。
    
    1:40

15. Scope
    
    

16. Return 

17.
18. 
