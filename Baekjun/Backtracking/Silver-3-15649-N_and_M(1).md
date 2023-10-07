# My Solution
## 1. Approach
I attempted to find all possible combinations using recursive functions. Here, I utilized an 'answer' array to store the values I intended to put in it. If the value I am trying to put in the answer array already exists, I avoided processing that part, thereby preventing the insertion of duplicate numbers.

## 2. Code
```python
n, m = tuple(map(int, input().split()))
answer = []

def sequence(num):
    if num == m:
        print(" ".join(map(str, answer)))
        return

    for i in range(1, n+1):
        if answer != [] and i in answer:
          continue
        answer.append(i)
        sequence(num+1)
        answer.pop()

sequence(0)
```

## 3. Self-feedback
I couldn't recall the approach to backtracking problems, so I wrote the code while reviewing the materials I studied on CodeTree. I realized that I haven't fully grasped the concept of backtracking yet, so I've decided that there is a need for further study. I plan to study it more to better understand the concept.

# Good Solution