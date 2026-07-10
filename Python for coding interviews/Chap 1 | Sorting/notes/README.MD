# Sorting 

## `.sort()`

### Main Points 

- sorts the element in the list in ascending order by default 
- for strings they are sorted in lexicographical order
- return value is `None`
- Time and Space Complexity 
  - Time Complexity : O(nlogn)
  - Space Complexity : O(n) 
    - n ➡️ n is the number of elements in the list 
  - `.sort()` uses Timsort algorithm for sorting lists 

### Function signature of `.sort()`

```python 
def sort (key =None, reverse = False) ->None: 
```

- key parameter ➡️ allows us to customize the sorting order 
- reverse parameter ➡️ boolean value that determines whether the list should be sorted in descending order .By default it is set to `False`

### Sorting a list in descending order 

- set the reverse parameter to `True`

  ```python
  elements = [5,3,6,2,1]
  elements.sort(key =None , reverse = True)
  print(elements) #[6,5,3,2,1]
  ```

- we can omit the key parameter 

  ```python
  elements.sort(reverse = True)
  ```

### Custom sort 

- key parameter 

  - allows us to specify a custom sorting order 

  - accepts a function that returns a value to be used for sorting 

    ```python
    def get_word_length(word:str)-> int:
      return len(word)
    
    words = ["apple","banana","kiwi","pear","watermelon","blueberry","cherry"]
    words.sort(key = get_word_length)
    print(words) # ["kiwi","pear","apple","banana","cherry","blueberry","watermelon"]
    ```

### Sort Lambda

- Lambda function syntax 

  - The keyword `lambda`
  - The input varibale word .We can use any variable name 
  - The colon `:` after which we define the function body 
  - The expression `len(word)` which is the return value of the function (It must be a single expression)

  ```python
  words =["apple","banana","kiwi","pear","watermelon","blueberry","cherry"]
  words.sort(key = lambda word:len(word))
  print(words) #["kiwi","pear","apple","banana","cherry","blueberry","watermelon"]
  ```

## `.sorted()`

- The `.sorted()` function returns a new list with the elements sorted in the specified order .The original list remains unchanged 

  ```python
  words =["kiwi","pear","apple","banana","cherry","blueberry"]
  sorted_words = sorted(words)
  print(sorted_words) # ["apple","banana","blueberry","cherry","kiwi","pear"]
  
  ```

- We can also specify the order using the `reverse` parameter 

  ```python  
  numbers = [5,-3,2,-4,6,-2,4]
  sorted_numbers = sorted(numbers , reverse = True)
  print(sorted_numbers) #[6,5,4,2,-2,-3,-4]
  ```

- We can also pass a custom function to the `key` parameter to specify the sorting criteria

  ```python
  numbers = [5,-3,2,-4,6,-2,4]
  sorted_numbers = sorted(numbers , key = abs)
  print(sorted_numbers) # [2,-2,-3,4,-4,5,6]
  ```

- For the most part its similar to the `sort()` method but it returns a new list instead of modifying the original list 