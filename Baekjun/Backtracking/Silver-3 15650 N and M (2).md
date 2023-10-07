# My Solution
## 1. Approach
I attempted to find all possible combinations using recursive functions. Here, I utilized an 'answer' array to store the values I intended to put in it. If the last value in the answer array is greater than the value you want to insert, I avoided processing that part. Thanks to this, I was able to output the values in the answer array arranged in ascending order.

## 2. Code
```python
n, m = tuple(map(int, input().split()))
answer = []

def sequence(num):
    if num == m:
        print(" ".join(map(str, answer)))
        return

    for i in range(1, n+1):
        if answer != [] and answer[-1] >= i:
          continue
        answer.append(i)
        sequence(num+1)
        answer.pop()

sequence(0)
```

## 3. Self-feedback
It's the same as the self-feedback mentioned in problem 15650 "N and M (1)".

# Good Solution