# JumpToPython4장

날짜: 2021년 6월 27일

# 함수

### 매개변수와 인수

- 매개변수(parameter)와 인수(arguments)는 혼용해서 사용되는 헷갈리는 용어이므로 잘 기억해 두자. 매개변수는 함수에 입력으로 전달된 값을 받는 변수를 의미하고 인수는 함수를 호출할 때 전달하는 입력값을 의미한다.

```python
def add(a, b):  # a, b는 매개변수
    return a+b

print(add(3, 4))  # 3, 4는 인수
```

### 입력값이 몇 개가 될지 모를때는?

```python
>>> def add_many(*args): 
...     result = 0 
...     for i in args: 
...         result = result + i 
...     return result 
... 
>>>
```

키워드 파라미터 kwargs

```python
>>> print_kwargs(a=1)
{'a': 1}
>>> print_kwargs(name='foo', age=3)
{'age': 3, 'name': 'foo'}
```

### [return의 또 다른 쓰임새]

```python
>>> def say_nick(nick): 
...     if nick == "바보": 
...         return 
...     print("나의 별명은 %s 입니다." % nick)

>>> say_nick('야호')
나의 별명은 야호입니다.
>>> say_nick('바보')
>>>
```

### 매개변수에 초깃값 미리 설정하기

```python
def say_myself(name, old, man=True): 
    print("나의 이름은 %s 입니다." % name) 
    print("나이는 %d살입니다." % old) 
    if man: 
        print("남자입니다.")
    else: 
        print("여자입니다.")

say_myself("박응용", 27)
say_myself("박응용", 27, True)
나의 이름은 박응용입니다.
나이는 27살입니다.
남자입니다.

입력값으로 "박응용", 27처럼 2개를 주면 name에는 "박응용"이 old에는 27이 대입된다.
 그리고 man이라는 변수에는 입력값을 주지 않았지만 초깃값 True를 갖게 된다.

say_myself("박응선", 27, False)
나의 이름은 박응선입니다.
나이는 27살입니다.
여자입니다.
```

# 파일 읽고 쓰기

### 파일 객체 = open(파일 이름, 파일 열기 모드)

![JumpToPython4%E1%84%8C%E1%85%A1%E1%86%BC%20eab0420ed88b4d4eafc5f35b6a144563/Untitled.png](JumpToPython4%E1%84%8C%E1%85%A1%E1%86%BC%20eab0420ed88b4d4eafc5f35b6a144563/Untitled.png)

### readline() 함수 이용하기

- f.open("새파일.txt", 'r')로 파일을 읽기 모드로 연 후 readline()을 사용해서 파일의 첫 번째 줄을 읽어 출력하는 경우

```python
# readline_test.py
f = open("C:/doit/새파일.txt", 'r')
line = f.readline()
print(line)
f.close()
```

### readlines() 함수 사용하기

- 파일의 모든 줄을 읽어서 각각의 줄을 요소로 갖는 리스트로 돌려준다.

### read() 함수 사용하기

- 파일의 내용 전체를 문자열로 돌려준다.