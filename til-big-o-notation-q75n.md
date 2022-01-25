# Big-O Notation

> Tuesday, January 25, 2022

## Common Complexities

* Linear O(n)
* Quadratic O(n<sup>2</sup>)
* Constant O(1)
* Exponential O(2<sup>N</sup>)
* Logarithmic O(log n)


## Linear

Complexity grows linearly over time.

Higher input == Higher Complexity

```python
n = 500
for i in range(n):
  print(i)
```

## Quadratic

Squares the number of inputs

```python
n = 500
for i in range(n):
  for j in range(n):
    print(i, j)
```

## Constant

No matter the input size, complexity remains the same

```python
fruits = ['banana', 'strawberries', 'oragne']
print(fruits[0]) # time accessing `fruits` array is constant
```

## Exponential

Complexity doubles with each addition to the input dataset.

e.g. looping over all possible combinations of an array

```python
def fibonacci(n):
  if (n <= 1):
    return n
  return fibonacci(n - 2) + fibonacci(n - 1)
```


## Logarithmic

Complexity goes up linearly while the input goes up exponentially

Next preferred complexity (constant being ideal).


```python
  print(i)
for i in range(n, step=i * 2):
```

Another example is binary search


---

_References_

* https://www.youtube.com/watch?v=Z0bH0cMY0E8
* https://roadmap.sh/guides/big-o-notation
