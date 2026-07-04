# Introduction 

Anki: 01-introduction

**Q**: How do we print `Hello , world!` in Python ? 

**Solution**:

```python
print("Hello, world!")
```

**Q**: Explain the difference between interpreted language and compiled language ? 
**Solution**: 

| interpreted language                                         | compiled language                                     |
| ------------------------------------------------------------ | ----------------------------------------------------- |
| code is executed line by line by an interpreter usually written in another language | code is translated into machine code before it is run |

**Q**: Is python an interpreted language or compiled language ? 

**Solution**:

Python is an interpreted language

**Q**: How can we print `They said "Hello , world"` in Python ? 

**Solution**: 

- backslash(/) tells python that we want to interpret the quote `"` as a character inside the string not as a quote that ends the srtring 

  ```python
  print("They said , \"Hello,world!\"")
  ```

**Q**: Explain the difference between Syntax Error , Runtime Error and Logical Error ? 

**Solution**:

| Syntax Error                                                 | Runtime Error                                                | Logical Error                                                |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| code not written according to rules of the programming language | error that occurs while the program is running <br />For example: if we programmed a calculator and the user tries to divide by zero we will get a runtime error | Error that occurs when the program runs without crashing or producing an error but the output is not what the programmer intended |

**Q**: How do we add comments in Python ? 

**Solution**:

Any text after the `#` character on a line is considered a comment and ignored by python 

```python
# This is a comment
```

