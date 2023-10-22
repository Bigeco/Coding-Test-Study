![제목 없음](https://github.com/Bigeco/Coding-Test-Study/assets/104182414/847be80e-368f-4624-8e68-8df821c561f6)

## Point
재귀함수를 잘 이해하기 위해서 스택 구조를 이해할 필요가 있었다. 기존에 알고는 있었지만 정확히 알고 있지 않았음을 깨닫게 되었는데, 구체적으로 말하자면 
시스템 관점에서 스택은 "Return Address" 를 가지고 있다. 
```python
def f(n):
    if n == 0:
        return 1
    return n * f(n-1)


n = int(input())
print(f(n))
```
예를 들어, f(n) 이 실행되면 그 f(n) 이 실행되었던 주소값이 있을 것이다. 즉, 그 함수가 호출이 되었던 그 자리로 다시 돌아가기 위해서는 "Return Address"가 반드시 필요하다. 
그래서 재귀 함수 동작 과정을 이해하는 과정에서 "Return Address"를 계속해서 의식하면서 이해했다.
