# Memoization and Dynamic Programming

> Tuesday, February 01, 2022

As far as I understand, _Memoization_ is another type of caching where we run a function, compute its results and cache them. That way we don't need to perform the calculations again and instead, we can just return the previously computed result from the cache.

A great example is Fibonacci:

```python
def fib(n):
  if n in {0, 1}:
    return n

  return fib(n - 1) + fib(n + 2)
```

So far the function looks good BUT we are wasting computing power because if we do `fib(10)`, we are computing `fib(8..2)` multiple times.

n = 10

fib(10) = fib(10 - 1 = 9) + fib(10 - 2 = 8)

fib(9) = fib(9 - 1 = 8) + fib(9 - 2 = 7)
...

The list goes on but as you can see, `fib(8)` is being computed twice and it's a waste of computing power since we already know what the result was for fib(8)

```python
fib_cache = {0: 0, 1: 1, }
def fib(n):
  if n in fib_cache:
    return fib_cache[n]
  cache[n] = fib(n - 1) + fib(n - 2)
  return cache[n]
```

Now we don't waste computing power, though we have an additional space requirement to store the results.

---

_References_

- https://www.youtube.com/watch?v=P8Xa2BitN3I
- https://stackoverflow.com/questions/6184869/what-is-the-difference-between-memoization-and-dynamic-programming
