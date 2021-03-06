# 기초

화면에 `Hello World`를 출력하는 것만으로는 부족하지요? 여러분은 아마 더 많은 것들을 해 보고 싶을 것입니다. 뭔가 정보를 입력받고, 처리한 뒤 결과물을 출력하는 프로그램을 만들고 싶으실 테지요. 파이썬에서는 상수들과 변수들을 이용하여 이러한 일을 할 수 있습니다. 이 장에서는 이외에도 몇 가지 기본 기능들에 대해서도 다뤄 볼 것입니다.

## 주석

주석은 `#` 문자 뒤에 따라오는 짧은 문장입니다. 주로 소스 코드를 읽는 사람들을 위해 주석을 남기는 용도로 빈번하게 사용됩니다.


예제:

```python
print('hello world') # Note that print is a function
```

또는

```python
# Note that print is a function
print('hello world')
```

여러분이 프로그램을 작성할 때, 주석을 가능한 많이 사용하시기 바랍니다.

- 미리 가정하고 넘어간 것들에 대한 설명
- 중요한 결정사항에 대한 설명
- 중요한 세부사항에 대한 설명
- 해결하고자 하는 문제에 대한 설명
- 앞으로 극복하려고 하는 문제들에 대한 설명 등등.

[코드는 어떻게? 라는 물음에 답하지만, 주석은 왜? 라는 물음에 답해야 합니다(영문)](http://www.codinghorror.com/blog/2006/12/code-tells-you-how-comments-tell-you-why.html).

주석은 여러분의 프로그램을 읽는 사람들에게 여러분이 작성한 프로그램이 무엇을 하는 프로그램인지 쉽게 파악할 수 있도록 도움을 주는 역할을 합니다. 프로그램을 작성하고 한 6개월쯤 뒤에는 여러분이 작성한 주석에 도움을 받는 사람이 여러분 자신이 될 수도 있다는 점을 꼭 기억하세요!

## 리터럴 상수

리터럴 상수는 `5`, `1.23`과 같은 숫자나, `'This is a string'` 혹은 `"It’s a string!"` 과 같은 문자열 등을 말합니다.

이것들이 리터럴 상수라고 불리우는 이유는 이것들이 프로그램 내에 직접 문자 형태로(literally) 지정되는 값들이기 때문입니다. 이러한 값들은 한 번 지정되면 변하지 않습니다. 예를 들면 숫자 `2`는 언제나 자기 자신이 2라는 숫자임을 나타내며 어떤 다른 의미도 갖지 않습니다. 이들은 한번 지정되면 그 값을 변경할 수 없기 때문에 _상수_입니다. 그 중에서도 특별히 이러한 값들을 리터럴 상수라고 부릅니다.

## 숫자형

숫자형에는 정수형(Integer)과 부동 소수점 숫자형(Float)의 두 가지 종류가 있습니다. 

정수형 숫자의 예는 `2`입니다. 이것은 단순히 2라는 숫자를 의미하는 것입니다. 부동 소수점 숫자의 예는 `3.23`, `52.3E-4`와 같은 값입니다. `E` 표기법은 E 뒤의 값이 10의 지수임을 나타냅니다. 예를 들어 `52.3E-4`는 `52.3 * 10^-4^`라는 값을 의미합니다.

> **숙련된 프로그래머들을 위한 주석**
> 
> 파이썬에서는 `long`형이 따로 없습니다. 대신 `int`형에 어떤 크기의 정수든지 담을 수 있습니다.

## 문자열

문자열이란 _문자_의 _나열_을 뜻합니다. 문자열은 간단하게 말하자면 문자들의 집합입니다. 여러분은 아마 앞으로 작성하게 될 거의 모든 파이썬 프로그램에서 문자열을 사용하게 될 것입니다. 따라서 아래 항목들을 주의깊게 살펴보세요.

### 작은 따옴표

여러분은 작은 따옴표를 이용하여 문자열을 지정할 수 있습니다. 예를 들어 `'Quote me on this'`와 같이 하면 됩니다. 모든 공백 문자, 즉 띄어쓰기나 탭 등은 입력한 그대로 유지됩니다.

### 큰 따옴표

큰 따옴표로 둘러싸인 문자열은 작은 따옴표로 둘러싸인 문자열과 완전히 동일하게 취급됩니다. 예를 들면, `"What’s your name?"`과 같습니다.(큰 따옴표로 둘러싸인 문자열 안에 작은 따옴표가 포함되어도 됩니다).

### 따옴표 세 개 {#triple-quotes}

여러 줄에 걸친 문자열은 세 개의 따옴표로 표현할 수 있습니다 - (`"""` 또는 `'''`). 세 개의 따옴표로 묶여진 문자열 안에서는 작은 따옴표든 큰 따옴표든 마음대로 사용할 수 있습니다. 예를 들면 다음과 같습니다.

```python
'''This is a multi-line string. This is the first line.
This is the second line.
"What's your name?," I asked.
He said "Bond, James Bond."
'''
```

### 문자열은 수정이 불가

여러분이 문자열을 한번 만들면, 그 문자열의 내용은 더이상 변경할 수 없습니다. 이것은 어떤 면에서는 좀 불편할 수 있다고 느낄 수 있겠습니다만, 사실은 그렇지 않습니다. 책의 뒷부분에서 여러 프로그램 예시를 통해 왜 이것이 큰 제약이 아닌지 살펴볼 것입니다.

> **C/C++ 프로그래머들을 위한 주석**
> 
> 파이썬에서는 `char`형이 따로 구분되어 있지 않습니다. 파이썬에서는 이것이 딱히 필요가 없습니다. 곧 여러분도 char 형을 찾지 않게 될 것입니다.

<!-- -->

> **Perl/PHP 프로그래머들을 위한 주석**
> 
> 파이썬에서는 작은 따옴표와 큰 따옴표로 둘러싸인 문자열을 동일하게 취급합니다. 둘 사이에 어떤 차이도 없습니다.

### 문자열 포맷팅

문자열을 생성하려고 할 때, 종종 다른 정보들을 포함하여 생성하고 싶을 때가 있습니다. 이것을 문자열 포맷팅이라고 하며, 이를 위해 `format()`을 이용합니다.

다음을 str_format.py 라는 이름으로 저장하세요.

```python
age = 20
name = 'Swaroop'

print('{0} was {1} years old when he wrote this book'.format(name, age))
print('Why is {0} playing with that python?'.format(name))
```

실행 결과:

```
$ python str_format.py
Swaroop was 20 years old when he wrote this book
Why is Swaroop playing with that python?
```

**동작 원리**

먼저 중괄호로 표현된 특별한 표시들이 포함된 문자열을 만들고, 그 후에 문자열의 `format` 메소드를 사용하여 이 표시들을 `format` 메소드에 주어진 인자들로 치환한 것입니다.

위 예시에서는 문자열 내에서 첫번째로 `{0}` 이 사용되었으며 이것은 format 메소드에 주어진 첫번째 인자, 즉 변수 `name`에 해당됩니다. 마찬가지로, 두번째 사용된 표시는 `{1}` 이며 이것은 format 메소드에 주어진 두번째 인자인 `age`에 해당됩니다. 파이썬은 숫자를 셀 때 항상 0 부터 세기 시작한다는 점에 유의하세요. 즉, 첫번째 인자의 인덱스는 0 이며, 두번째는 1 입니다.

또한 다음과 같이 문자열 더하기를 이용하여 동일한 결과를 얻을 수도 있습니다.

```python
name + ' is ' + str(age) + ' years old'
```

그러나 이것은 척 보기에도 깔끔하지 못하며, 작성 중 실수하기도 쉽습니다. 또 이 경우 각 변수를 일일이 명시적으로 문자열로 변환해주어야 하지만, `format` 메소드를 이용할 경우에는 알아서 자동으로 변환해 줍니다. 또 `format` 메소드를 이용할 경우 변수들을 신경쓰지 않고 문자열의 내용을 수정하기 쉽고, 문자열에 신경쓰지 않고도 변수의 위치나 순서 등을 변경하기가 더 쉽습니다.

이 때 중괄호 내에 주어진 숫자는 생략할 수 있습니다. 다음 예제를 확인하세요.

```python
age = 20
name = 'Swaroop'

print('{} was {} years old when he wrote this book'.format(name, age))
print('Why is {} playing with that python?'.format(name))
```

위 프로그램 또한 동일한 결과를 출력합니다.

파이썬의 `format`은 중괄호 표시의 위치에 주어진 인자들의 값을 치환해 넣습니다. 이때, 중괄호 표시에 다음과 같이 좀 더 상세히 세부사항을 지정할 수도 있습니다.

```python
# 소수점 이하 셋째 자리까지 부동 소숫점 숫자 표기 (0.333)
print('{0:.3f}'.format(1.0/3))
# 밑줄(_)로 11칸을 채우고 가운데 정렬(^)하기 (___hello___)
print('{0:_^11}'.format('hello'))
# 사용자 지정 키워드를 이용해 (Swaroop wrote A Byte of Python) 표기
print('{name} wrote {book}'.format(name='Swaroop', book='A Byte of Python'))
```

실행 결과:

```
0.333
___hello___
Swaroop wrote A Byte of Python
```

지금까지 문자열 포맷팅에 대해 알아보았습니다. 여기서 `print` 명령은 언제나 주어진 문자열의 끝에 "줄바꿈" 문자 (`\n`) 을 덧붙인다는 것 또한 기억하세요. 따라서 `print` 명령을 호출할 때마다 인자로 주어진 내용들은 항상 그 다음 줄에 출력됩니다. 이것을 막기 위해서는 print 함수의 인자 `end`를 공백으로 지정하면 됩니다.
```python
print('a', end='')
print('b', end='')
```

실행 결과:

```
ab
```

또는 `end`를 한 칸 띄운 값으로 지정해도 됩니다.

```python
print('a', end=' ')
print('b', end=' ')
print('c')
```

실행 결과:

```
a b c
```

### Escape Sequences

Suppose, you want to have a string which contains a single quote (`'`), how will you specify this string? For example, the string is `"What's your name?"`. You cannot specify `'What's your name?'` because Python will be confused as to where the string starts and ends. So, you will have to specify that this single quote does not indicate the end of the string. This can be done with the help of what is called an _escape sequence_. You specify the single quote as `\'` : notice the backslash. Now, you can specify the string as `'What\'s your name?'`.

Another way of specifying this specific string would be `"What's your name?"` i.e. using double quotes. Similarly, you have to use an escape sequence for using a double quote itself in a double quoted string. Also, you have to indicate the backslash itself using the escape sequence `\\`.

What if you wanted to specify a two-line string? One way is to use a triple-quoted string as shown [previously](#triple-quotes) or you can use an escape sequence for the newline character - `\n` to indicate the start of a new line. An example is:

```python
'This is the first line\nThis is the second line'
```

Another useful escape sequence to know is the tab: `\t`. There are many more escape sequences but I have mentioned only the most useful ones here.

One thing to note is that in a string, a single backslash at the end of the line indicates that the string is continued in the next line, but no newline is added. For example:

```python
"This is the first sentence. \
This is the second sentence."
```

is equivalent to

```python
"This is the first sentence. This is the second sentence."
```

### Raw String

If you need to specify some strings where no special processing such as escape sequences are handled, then what you need is to specify a _raw_ string by prefixing `r` or `R` to the string. An example is:

```python
r"Newlines are indicated by \n"
```

> **Note for Regular Expression Users**
> 
> Always use raw strings when dealing with regular expressions. Otherwise, a lot of backwhacking may be required. For example, backreferences can be referred to as `'\\1'` or `r'\1'`.

## Variable

Using just literal constants can soon become boring - we need some way of storing any information and manipulate them as well. This is where _variables_ come into the picture. Variables are exactly what the name implies - their value can vary, i.e., you can store anything using a variable. Variables are just parts of your computer's memory where you store some information. Unlike literal constants, you need some method of accessing these variables and hence you give them names.

## Identifier Naming

Variables are examples of identifiers. _Identifiers_ are names given to identify _something_. There are some rules you have to follow for naming identifiers:

- The first character of the identifier must be a letter of the alphabet (uppercase ASCII or lowercase ASCII or Unicode character) or an underscore (`_`).
- The rest of the identifier name can consist of letters (uppercase ASCII or lowercase ASCII or Unicode character), underscores (`_`) or digits (0-9).
- Identifier names are case-sensitive. For example, `myname` and `myName` are _not_ the same. Note the lowercase `n` in the former and the uppercase `N` in the latter.
- Examples of _valid_ identifier names are `i`, `name_2_3`. Examples of _invalid_ identifier names are `2things`, `this is spaced out`, `my-name` and `>a1b2_c3`.

## Data Types

Variables can hold values of different types called _data types_. The basic types are numbers and strings, which we have already discussed. In later chapters, we will see how to create our own types using [classes](./oop.md#classes).

## Object

Remember, Python refers to anything used in a program as an _object_.  This is meant in the generic sense. Instead of saying "the _something_"', we say "the _object_".

> **Note for Object Oriented Programming users**:
>
> Python is strongly object-oriented in the sense that everything is an object including numbers, strings and functions.

We will now see how to use variables along with literal constants. Save the following example and run the program.

## How to write Python programs

Henceforth, the standard procedure to save and run a Python program is as follows:

### For PyCharm

1. Open [PyCharm](./first_steps.md#pycharm).
2. Create new file with the filename mentioned.
3. Type the program code given in the example.
4. Right-click and run the current file.

NOTE: Whenever you have to provide [command line arguments](./modules.md#modules), click on `Run` -> `Edit Configurations` and type the arguments in the `Script parameters:` section and click the `OK` button:

![PyCharm command line arguments](./img/pycharm_command_line_arguments.png)

### For other editors

1. Open your editor of choice.
2. Type the program code given in the example.
3. Save it as a file with the filename mentioned.
4. Run the interpreter with the command `python program.py` to run the program.

### Example: Using Variables And Literal Constants

Type and run the following program:

```python
# Filename : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''This is a multi-line string.
This is the second line.'''
print(s)
```

Output:

```
5
6
This is a multi-line string.
This is the second line.
```

**How It Works**

Here's how this program works. First, we assign the literal constant value `5` to the variable `i` using the assignment operator (`=`). This line is called a statement because it states that something should be done and in this case, we connect the variable name `i` to the value `5`. Next, we print the value of `i` using the `print` statement which, unsurprisingly, just prints the value of the variable to the screen.

Then we add `1` to the value stored in `i` and store it back. We then print it and expectedly, we get the value `6`.

Similarly, we assign the literal string to the variable `s` and then print it.

> **Note for static language programmers**
> 
> Variables are used by just assigning them a value. No declaration or data type definition is needed/used.

## Logical And Physical Line

A physical line is what you _see_ when you write the program. A logical line is what _Python sees_ as a single statement. Python implicitly assumes that each _physical line_ corresponds to a _logical line_.

An example of a logical line is a statement like `print 'hello world'` - if this was on a line by itself (as you see it in an editor), then this also corresponds to a physical line.

Implicitly, Python encourages the use of a single statement per line which makes code more readable.

If you want to specify more than one logical line on a single physical line, then you have to explicitly specify this using a semicolon (`;`) which indicates the end of a logical line/statement. For example:

```python
i = 5
print(i)
```

is effectively same as

```python
i = 5;
print(i);
```

which is also same as

```python
i = 5; print(i);
```

and same as

```python
i = 5; print(i)
```

However, I *strongly recommend* that you stick to *writing a maximum of a single logical line on each single physical line*. The idea is that you should never use the semicolon. In fact, I have _never_ used or even seen a semicolon in a Python program.

There is one kind of situation where this concept is really useful: if you have a long line of code, you can break it into multiple physical lines by using the backslash. This is referred to as _explicit line joining_:

```python
s = 'This is a string. \
This continues the string.'
print(s)
```

Output:

```
This is a string. This continues the string.
```

Similarly,

```python
i = \
5
```

is the same as

```python
i = 5
```

Sometimes, there is an implicit assumption where you don't need to use a backslash. This is the case where the logical line has a starting parentheses, starting square brackets or a starting curly braces but not an ending one. This is called *implicit line joining*. You can see this in action when we write programs using [list](./data_structures.md#lists) in later chapters.

## Indentation

Whitespace is important in Python. Actually, *whitespace at the beginning of the line is important*. This is called _indentation_. Leading whitespace (spaces and tabs) at the beginning of the logical line is used to determine the indentation level of the logical line, which in turn is used to determine the grouping of statements.

This means that statements which go together _must_ have the same indentation. Each such set of statements is called a *block*. We will see examples of how blocks are important in later chapters.

One thing you should remember is that wrong indentation can give rise to errors. For example:

```python
i = 5
# Error below! Notice a single space at the start of the line
 print('Value is', i)
print('I repeat, the value is', i)
```

When you run this, you get the following error:

```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```

Notice that there is a single space at the beginning of the second line. The error indicated by Python tells us that the syntax of the program is invalid i.e. the program was not properly written. What this means to you is that _you cannot arbitrarily start new blocks of statements_ (except for the default main block which you have been using all along, of course). Cases where you can use new blocks will be detailed in later chapters such as the [control flow](./control_flow.md#control_flow).

> **How to indent**
> 
> Use four spaces for indentation. This is the official Python language recommendation. Good editors will automatically do this for you. Make sure you use a consistent number of spaces for indentation, otherwise your program will not run or will have unexpected behavior.

<!-- -->

> **Note to static language programmers**
> 
> Python will always use indentation for blocks and will never use braces. Run `from __future__ import braces` to learn more.

## Summary

Now that we have gone through many nitty-gritty details, we can move on to more interesting stuff such as control flow statements. Be sure to become comfortable with what you have read in this chapter.
