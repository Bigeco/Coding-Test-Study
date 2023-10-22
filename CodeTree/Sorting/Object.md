```
class Student:
    def __init__(self, kor, eng, math):
        self.kor = kor
        self.eng = eng
        self.math = math

students = [
    Student(90, 80, 90),
    Student(20, 80, 80),
    Student(90, 30, 60),
    Student(60, 10, 50),
    Student(80, 20, 10)
]
```


## 오름차순 정렬
```
students.sort(key=lambda x: x.kor)
students = sorted(students, key=lambda x: x.kor)
```


## 내림차순 정렬
```
students.sort(key=lambda x: -x.kor)
students = sorted(students, key=lambda x: -x.kor)
```
