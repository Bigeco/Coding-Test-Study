![제목 없음](https://github.com/Bigeco/Coding-Test-Study/assets/104182414/20e01dfc-d530-4085-946d-dd70e98fe9bf)


## 비효율적인 코드 
![제목 없음](https://github.com/Bigeco/Coding-Test-Study/assets/104182414/36e638ce-ffdd-41e2-b4a6-d987fdbc9173)


## 규칙성 발견하기 
```python
if dir_num == 0:
    nx, ny = x + 1, y + 0
elif dir_num == 1:
    nx, ny = x + 0, y - 1
elif dir_num == 2:
    nx, ny = x - 1, y + 0
else:
    nx, ny = x + 0, y + 1
```

## Main Idea
코드를 짤 때 눈여겨 보면 좋은 것은 '반복되는 코드'를 찾는 것이다. 즉 **Clean Code** 를 작성하기 위해서는 반복되는 코드를 줄여야 하는 것이다. 
위 코드의 경우 어떤 방향을 가냐에 따라서 x 값과 y 값에 더해지는 값이 존재하는데, 이 값은 변하지 않는 '상수' 값에 해당한다. 

## 해결
```
dx = [1, 0, -1, 0]
dy = [0, -1, 0, 1]

nx, ny = x + dx[dir_num], y + dy[dir_num]
```
다음과 같이 if 문을 사용해서 8줄을 적은 것을 단 1줄 만에 줄여낼 수 있다. 
