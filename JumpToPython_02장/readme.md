# JumpToPython2장

날짜: 2021년 6월 22일

## 문자열 안에 작은따옴표나 큰따옴표를 포함시키고 싶을 때

- 이럴 때는 다음과 같이 문자열을 큰따옴표(")로 둘러싸야 한다. 큰따옴표 안에 들어 있는 작은따옴표는 문자열을 나타내기 위한 기호로 인식되지 않는다. 반대로 큰따옴표를 넣고 싶다면 작은따옴표로 감싸면 된다.

```python
food = "Python's favorite food is perl"
```

- 백슬래시(\)를 사용해서 작은따옴표(')와 큰따옴표(")를 문자열에 포함시키기. 백슬래시(\)를 작은따옴표(')나 큰따옴표(") 앞에 삽입하면 백슬래시(\) 뒤의 작은따옴표(')나 큰따옴표(")는 문자열을 둘러싸는 기호의 의미가 아니라 문자 ('), (") 그 자체를 뜻하게 된다.

```python
food = 'Python\'s favorite food is perl'
say = "\"Python is very easy.\" he says."
```

## 여러 줄인 문자열을 변수에 대입하고 싶을 때

1. 줄을 바꾸기 위한 이스케이프 코드 \n 삽입하기

```python
multiline = "Life is too short\nYou need python"
```

2. 연속된 작은따옴표 3개(''') 또는 큰따옴표 3개(""") 사용하기

```python
multiline = """
Life is too short
You need python
"""
```

![JumpToPython2%E1%84%8C%E1%85%A1%E1%86%BC%2072b5a504bd7b45208a74b02b8c3f13a8/Untitled.png](JumpToPython2%E1%84%8C%E1%85%A1%E1%86%BC%2072b5a504bd7b45208a74b02b8c3f13a8/Untitled.png)

["Pithon"이라는 문자열을 "Python"으로 바꾸려면?]

```python
a = "Pithon"
a[1]
'i'
a[1] = 'y'
```

[포매팅 연산자 %d와 %를 같이 쓸 때는 %%를 쓴다]

```python
"Error is %d%%." % 98
'Error is 98%.'
```

## format 함수를 사용한 포매팅

1. 숫자 바로 대입

```python
"I eat {} apple.".format(3)
```

2. 문자열 바로 대입

```python
"I eat {0} apples".format("five")
```

3. 숫자 값을 가진 변수로 대입

```python
>>> number = 3
>>> "I eat {0} apples".format(number)
'I eat 3 apples'
```

4. 2개 이상의 값 넣기

```python
>>> number = 10
>>> day = "three"
>>> "I ate {0} apples. so I was sick for {1} days.".format(number, day)
'I ate 10 apples. so I was sick for three days.'
```

5. 이름으로 넣기

```python
>>> "I ate {number} apples. so I was sick for {day} days.".format(number=10, day=3)
'I ate 10 apples. so I was sick for 3 days.'
```

## f 문자열 포매팅

```python
>>> name = '홍길동'
>>> age = 30
>>> f'나의 이름은 {name}입니다. 나이는 {age}입니다.'
'나의 이름은 홍길동입니다. 나이는 30입니다.'
```

딕셔너리는 Key와 Value라는 것을 한 쌍으로 갖는 자료형이다.

```python
>>> d = {'name':'홍길동', 'age':30}
>>> f'나의 이름은 {d["name"]}입니다. 나이는 {d["age"]}입니다.'
'나의 이름은 홍길동입니다. 나이는 30입니다.'
```

## 문자열 관련 함수들

1. 문자 개수 세기

```python
>>> a = "hobby"
>>> a.count('b')
2
```

2. 위치 알려주기(존재하지 않은 문자는 -1을 반환한다.)

```python
>>> a = "Python is the best choice"
>>> a.find('b')
14
>>> a.find('k')
-1
```

3. 위치 알려주기2(index)

```python
>>> a = "Life is too short"
>>> a.index('t')
8
```

4. 문자열 삽입(join)

```python
>>> ",".join('abcd')
'a,b,c,d'
```

5. 왼쪽 공백지우기(lstrip)

```python
>>> a = " hi "
>>> a.lstrip()
'hi '
```

6.오른쪽 공백지우기(rstrip)

```python
>>> a= " hi "
>>> a.rstrip()
' hi'
```

7. 양쪽 공백지우기(strip)

```python
>>> a = " hi "
>>> a.strip()
'hi'
```

8. 문자열 바꾸기(replace)

```python
>>> a = "Life is too short"
>>> a.replace("Life", "Your leg")
'Your leg is too short'
```

9. 문자열 나누기(split)

```python
>>> a = "Life is too short"
>>> a.split()
['Life', 'is', 'too', 'short']
>>> b = "a:b:c:d"
>>> b.split(':')
['a', 'b', 'c', 'd']
```
