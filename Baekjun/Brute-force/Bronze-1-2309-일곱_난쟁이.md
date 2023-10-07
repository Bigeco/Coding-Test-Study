# My Solution
## 1. Approach
Due to the limited size of the array being searched, which is restricted to 9, I solved the problem using the "Bruth-force" method. At the end, since the 7 values need to be output in sorted order, I pre-sorted them in ascending order beforehand. The variables 'i' and 'j' represent the indices of the array values that are not to be added. The reason for having two variables is that we need to exclude two dwarfs from the total of nine.

## 2. Code
```python
arr = [
    int(input())
    for i in range(9)
]
arr.sort()

for i in range(9):
    for j in range(i+1, 9):
        sum_val = sum(arr) - (arr[i] + arr[j])
        if sum_val == 100:
            idx = [i, j]

for i in range(9):
    if i not in idx:
        print(arr[i])
```

## 3. Self-feedback


# Good Solution