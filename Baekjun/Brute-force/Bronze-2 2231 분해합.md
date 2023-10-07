# My Solution
## 1. Approach
To find the smallest decomposable sum, I needed the sum of each digit. Since I didn't know the number of digits before receiving input, I converted it to a string object and then to a list object to solve the problem. As I needed to find the minimum decomposable value, I immediately returned the result once I found it.

## 2. Code
```python
n = int(input())

def min_ctor(n):
    ans = 0
    for i in range(1, n):
        if i + sum(list(map(int, list(str(i))))) == n:
            ans = i
            return ans
    return ans

print(min_ctor(n))
```

## 3. Self-feedback
I realized there was no need to define a function after looking at someone else's solution. My code ended up unnecessarily consuming stack memory. Moreover, the process of converting it to a list object was not necessary.

# Good Solution
```python
n = int(input())
ans = 0

for i in range(1, n):
    if i + sum((map(int, str(i)))) == n:
        ans = i
        break

print(min_ctor(n))
```