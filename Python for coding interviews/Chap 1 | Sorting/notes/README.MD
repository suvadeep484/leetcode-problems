# Sorting 

## .sort() 

- we can sort a list of elements by calling `.sort()` on the list . It sorts the elements in *ascending order in-place* . The return value of the `.sort()` mwthod is `None`.for strings they are sorted in lexicographical order  

- Time and Space Complexity 

  - Time Complexity : O(nlogn)
  - Space Complexity : O(n)
  - n ➡️ number of elements in the list 

- Python uses Timsort algorithm for sorting lists

- Function signature of `.sort()` 

  ```python
  def sort (key =None , reverse = False) -> None
  ```

  - key parameter allows us to customize the sorting order 

  - reverse parameter is a boolean value that determines whether the list should be sorted in *descending order* .By default it is set to `False`

  - If we want to sort a list in descending order , we can set the `reverse` parameter to `True`

    ```python
    elements = [5, 3, 6, 2, 1]
    
    elements.sort(key=None, reverse=True)
    
    print(elements) # [6, 5, 3, 2, 1]
    ```

  - We can actually omit the `key` parameter and only pass the `reverse` parameter, by using a feature of Python called *keyword arguments*.

    ```python
    elements.sort(reverse=True)
    
    ```

  ## Sort Custom

  - the `key` parameter allows us to specify a custom sorting order. The `key` parameter accepts a function that returns a value to be used for sorting 

  - Example ➡️

    ```python
    def get_word_length(word: str) -> int:
        return len(word)
    
    words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]
    
    words.sort(key=get_word_length)
    
    print(words) # ['kiwi', 'pear', 'apple', 'banana', 'cherry', 'blueberry', 'watermelon']
    ```

    

## Sort Lambda 

Lambda function syntax ➡️

```python
words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]

words.sort(key=lambda word: len(word))

print(words) # ['kiwi', 'pear', 'apple', 'banana', 'cherry', 'blueberry', 'watermelon']
```

The syntax includes:

- The keyword `lambda`.
- The input variable `word`. We can use any variable name here.
- The colon `:`, after which we define the function body.
- The expression `len(word)`, which is the return value of the function.

A lambda function must be a single expression, and it cannot contain multiple statements.

## Sorted Copy 

- `sorted()`

  - The `sorted()` function returns a *new list* with the elements sorted in the specified order. The original list remains unchanged.

    ```python
    words = ["kiwi", "pear", "apple", "banana", "cherry", "blueberry"]
    
    sorted_words = sorted(words)
    
    print(sorted_words) # ['apple', 'banana', 'blueberry', 'cherry', 'kiwi', 'pear']
    ```

  - The `sorted()` function takes the list as the first argument and returns a new list with the elements sorted in ascending order by default

  - For the most part, it's similar to the `sort()` method, but it returns a new list instead of modifying the original list.