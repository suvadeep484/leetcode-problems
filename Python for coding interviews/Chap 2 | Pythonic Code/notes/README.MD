# Pythonic Code 

## Unpacking 

```python
point1= [0,0]
point2 = [2,4]
x1,y1 = point1 # x1 = 0 , y1 = 0
x2,y2 = point2 # x2 = 2 , y2 = 4
```

- We have 2 variables on the left side of the assignment operator with a list on the right side .This is called unpacking . We know point1 and point2 are lists of size 2 so we can unpack into two variables each
- Unpacking also works with tuples and sets with the same syntax

Note ➡️ we must have enough variables on the left side .

## Loop unpacking 

- we can also use unpacking in loops over a list of lists .This is useful when we know the size of the inner lists and want to unpack them into variables 

  ```python
  points = [[0,0],[2,4],[3,6],[5,10]]
  for x,y in points:
  	print(x,y)
  ```

## Enumerate 

- Suppose we wanted to loop over an array and we needed to access both the index and the element at that index .The Pythonic way to do this is to use the `enumerate()` function 

- The `enumerate()` function returns a tuple of the index and the element at that index .we can unpack this tuple into 2 variables in the for loop 

  ```python  
  nums = [2,7,9,2]
  for i,n in enumerate():
    print(i,n)
  ```

## Zip 

- Python provides an easy way to iterate over multiple lists at the same time using the `zip()` function .The `zip()` function takes multiple lists as arguments and returns an iterator of tuples .Each tuple contains an element from each list 

- This is useful when we have multiple lists of the same length and want to iterate over them together 

  ```python
  names =["Alice","Bob","Charlie","David"]
  scores = [90,85,88,92]
  for name,score in zip(names,scores):
    print(f"{name} scored {score}")
  ```

## Inequality 

- Python allows us to take a small shortcut when making multiple comparisions.The following code

  ```python
  x = 5 
  if 0<x and x<10:
    print("x is between 0 and 10")
  ```

  is equivalent to 

  ```python
  x = 5
  if 0<x<10:
    print("x is between 0 and 10")
  ```

  