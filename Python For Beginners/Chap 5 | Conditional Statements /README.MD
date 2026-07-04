# Conditional Statements 

## Comparison Operators 

- The comparision operators are: 
  - `==` Equal to
  - `!=` Not equal to
  - `<` Less than
  - `>` Greater than
  - `<=` Less than or equal to
  - `>=` Greater than or equal to

## If Statements 

```python
def is_account_overdraw(balance: int):
    if account_balance < 0:
        print("Your account is overdrawn.")
```

## If Statement Scope

- Unlike functions, `if` statements do not create a new scope. This means that variables defined inside an `if` statement are accessible outside of the `if` statement. Here's an example:

  ```python
  if True:
      message = "Hello"
  
  print(message)  # This will print "Hello"
  ```

- They can also update variables that were defined outside of the `if` statement. Here's an example:

  ```py
  balance = -100
  
  if balance < 0:
      balance = 0
  
  print(balance)  # This will print 0
  ```

  