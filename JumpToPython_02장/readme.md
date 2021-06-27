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
# 리스트 수정과 삭제

### del 함수 사용해 리스트 요소 삭제하기

```python
>>> a = [1, 2, 3]
>>> del a[1]
>>> a
[1, 3]
```

### 리스트에 요소 추가

```python
>>> a = [1, 2, 3, 4]
>>> a.append([5,6])
>>> a
[1, 2, 3, 4, [5, 6]]
```

### 리스트 정렬(sort)

```python
>>> a = [1, 4, 3, 2]
>>> a.sort()
>>> a
[1, 2, 3, 4]
#문자인 알파벳
>>> a = ['a', 'c', 'b']
>>> a.sort()
>>> a
['a', 'b', 'c']
```

### 리스트 뒤집기(reverse)

```python
>>> a = ['a', 'c', 'b']
>>> a.reverse()
>>> a
['b', 'c', 'a']
```

### 위치 반환(리스트에 있는 값을 검색해야 나옴)

```python
>>> a = [1,2,3]
>>> a.index(3)
2
>>> a.index(1)
0
```

### 리스트에 요소 삽입(insert)

insert(a, b)는 리스트의 a번째 위치에 b를 삽입하는 함수이다. 파이썬에서는 숫자를 0부터 센다는 것을 반드시 기억하자.

```python
>>> a = [1, 2, 3]
>>> a.insert(0, 4)
>>> a
[4, 1, 2, 3]
```

### 리스트 요소 제거(remove) (이것도 리스트에 있는 값을 직접 넣어 삭제해야함)

a가 3이라는 값을 2개 가지고 있을 경우 첫 번째 3만 제거되는 것을 알 수 있다.

```python
>>> a = [1, 2, 3, 1, 2, 3]
>>> a.remove(3)
>>> a
[1, 2, 1, 2, 3]
```

### 리스트 요소 끄집어내기(pop)

- pop()은 리스트의 맨 마지막 요소를 돌려주고 그 요소는 삭제한다.

```python
>>> a = [1,2,3]
>>> a.pop()
3
>>> a
[1, 2]
```

- pop(x)는 리스트의 x번째 요소를 돌려주고 그 요소는 삭제한다.

```python
>>> a = [1,2,3]
>>> a.pop(1) #인덱스 번호로 삭제
2
>>> a
[1, 3]
```

### 리스트 확장(extend)

- extend(x)에서 x에는 리스트만 올 수 있으며 원래의 a 리스트에 x 리스트를 더하게 된다.

```python
>>> a = [1,2,3]
>>> a.extend([4,5])
>>> a
[1, 2, 3, 4, 5]
>>> b = [6, 7]
>>> a.extend(b)
>>> a
[1, 2, 3, 4, 5, 6, 7]
```

# 튜플자료형

- 리스트와 아주 비슷한 형태이지만 수정과 삭제를 못한다는 점이 가장 큰 차이점

```python
>>> t1 = ()
>>> t2 = (1,)
>>> t3 = (1, 2, 3)
>>> t4 = 1, 2, 3
>>> t5 = ('a', 'b', ('ab', 'cd'))
```

t2 = (1,)처럼 단지 1개의 요소만을 가질 때는 요소 뒤에 콤마(,)를 반드시 붙여야 한다는 것과 t4 = 1, 2, 3처럼 괄호( )를 생략해도 무방하다는 점이다.

# 딕셔너리 자료형

### 딕셔너리 쌍 추가하기

- values값에 리스트를 삽입할 수 있음.

```python
>>> a = {1: 'a'}
>>> a[2] = 'b'
>>> a
{1: 'a', 2: 'b'}

>>> a['name'] = 'pey'
>>> a
{1: 'a', 2: 'b', 'name': 'pey'}

>>> a[3] = [1,2,3]
>>> a
{1: 'a', 2: 'b', 'name': 'pey', 3: [1, 2, 3]}
```

### 딕셔너리 요소 삭제하기

- 딕셔너리의 키를 불러옴으로써 삭제함(values값도 같이 삭제)

```python
>>> del a[1]
>>> a
{2: 'b', 'name': 'pey', 3: [1, 2, 3]}
```

### 딕셔너리 key를 사용해 value값 얻기

```python
>>> grade = {'pey': 10, 'julliet': 99}
>>> grade['pey']
10
>>> grade['julliet']
99
```

### Key로 Value얻기(get)

a['nokey']는 Key 오류를 발생시키고 a.get('nokey')는 None을 돌려준다는 차이가 있다.

```python
>>> a = {'name':'pey', 'phone':'0119993323', 'birth': '1118'}
>>> a.get('name')
'pey'
>>> a.get('phone')
'0119993323'

>>>>>>>>>>>>차이보기>>>>>>>>>>>>>>>>>
>>> a = {'name':'pey', 'phone':'0119993323', 'birth': '1118'}
>>> print(a.get('nokey'))
None
>>> print(a['nokey'])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'nokey'
```

---

## 딕셔너리 관련 함수들

### key리스트 만들기(keys)

```python
>>> a = {'name': 'pey', 'phone': '0119993323', 'birth': '1118'}
>>> a.keys()
dict_keys(['name', 'phone', 'birth'])
```

### Value 리스트 만들기(values)

```python
>>> a.values()
dict_values(['pey', '0119993323', '1118'])
```

### Key, Value 쌍 얻기(items)

```python
>>> a.items()
dict_items([('name', 'pey'), ('phone', '0119993323'), ('birth', '1118')])
```

### Key: Value 쌍 모두 지우기(clear)

clear 함수는 딕셔너리 안의 모든 요소를 삭제한다. 빈 리스트를 [ ], 빈 튜플을 ( )로 표현하는 것과 마찬가지로 빈 딕셔너리도 { }로 표현한다.

```python
>>> a = {'name': 'pey', 'phone': '0119993323', 'birth': '1118'}
>>> a.clear()
>>> a
{}
```

### 해당 Key가 딕셔너리 안에 있는지 조사하기(in)

```python
>>> a = {'name':'pey', 'phone':'0119993323', 'birth': '1118'}
>>> 'name' in a
True
>>> 'email' in a
False
```

# 집합자료형

- 중복 허용 안함
- 순서가 없음 > 인덱싱으로 값을 얻을 수 없음 > 리스트나 튜플로 변환한 후 가능

```python
>>> s2 = set("Hello")
>>> s2
{'e', 'H', 'l', 'o'}
```

### 교집합

- & 과  intersection함수를 이용하면 교집합을 얻을 수 있음.

```python
>>> s1 = set([1, 2, 3, 4, 5, 6])
>>> s2 = set([4, 5, 6, 7, 8, 9])
>>> s1 & s2
{4, 5, 6}
>>> s1.intersection(s2)
{4, 5, 6}
```

### 합집합

- |  과 union함수를 사용하면 됌

```python
>>> s1 | s2
{1, 2, 3, 4, 5, 6, 7, 8, 9}
>>> s1.union(s2)
{1, 2, 3, 4, 5, 6, 7, 8, 9}
```

### 차집합

- -부호와 difference 를 사용하여 차집합을 구한다.

```python
>>> s1 - s2
{1, 2, 3}
>>> s2 - s1
{8, 9, 7}
```

---

## 집합 자료형 관련 함수들

### 값 한개 추가하기(add)

```python
>>> s1 = set([1, 2, 3])
>>> s1.add(4)
>>> s1
{1, 2, 3, 4}
```

### 값 여러개 추가하기(update)

```python
>>> s1 = set([1, 2, 3])
>>> s1.update([4, 5, 6])
>>> s1
{1, 2, 3, 4, 5, 6}
```

### 특정 값 제거하기(remove)

```python
>>> s1 = set([1, 2, 3])
>>> s1.remove(2)
>>> s1
{1, 3}
```

