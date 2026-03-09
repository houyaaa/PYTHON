# Python 1주차 정규 과제 

📌Python 정규과제는 매주 정해진 분량의 『*파이썬 라이브러리를 활용한 데이터 분석*』 을 읽고 학습하는 것입니다. 이번주는 아래의 **Python_1st_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 참고 자료를 통해 보완하는 것이 좋습니다.

**교재 실습 예제 파일은 07_Python_Template 레포지토리의 notebooks 폴더에 업로드되어 있습니다.**

**👀(수행 인증샷은 필수입니다.)** 

## Python_1st_TIL

### 1장 시작하기 전에
#### 1. 다루는 내용
#### 2. 데이터 분석에 파이썬을 사용하는 이유
#### 3. 필수 파이썬 라이브러리
#### 4. 설치 및 설정
#### 5. 커뮤니티와 콘퍼런스
#### 6. 이 책을 살펴보는 방법
### 2장 파이썬 기초, IPython과 주피터 노트북 
#### 1. 파이썬 인터프리터 
#### 2. IPython 기초 
#### 3. 파이썬 기초
#### 4. 마치며


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.25~82    | ✅         |
| 2주차 | p.83~129   | 🍽️         |
| 3주차 | p.131~179  | 🍽️         |
| 4주차 | p.181~246 | 🍽️         |
| 5주차 | p.247~309 | 🍽️         |
| 6주차 | p.310~379 | 🍽️         |
| 7주차 | p.381~465 | 🍽️         |


<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 학습 내용 정리

## 1. 설치 및 설정 

```
아나콘다(Anaconda) 또는 미니콘다(Miniconda)를 설치한 후, 필수 패키지를 설치하고 설치 완료 화면을 캡처하여 제출해주세요.
```
<img width="962" height="742" alt="image" src="https://github.com/user-attachments/assets/685f908d-7d05-4aa0-9ecf-a483e422c3c2" />



## 2. 파이썬 인터프리터 

```
간단한 hello_world.py 파일을 생성한 후, Anaconda Prompt(또는 Miniconda Prompt)를 실행하세요.
(해당 파일에는 print('Hello World!')라고 입력해주세요.)
프롬프트에서 ipython을 입력하여 IPython 환경을 실행한 뒤, %run hello_world.py 명령어로 파일을 실행하시기 바랍니다.
실행 결과가 나타난 화면을 캡처하여 제출해주세요.
```
<img width="913" height="525" alt="image" src="https://github.com/user-attachments/assets/bea6671e-722d-49f8-b514-e3de1acdb4d7" />



## 3. IPython 기초  

### IPython 셀 실행하기 
```
IPython을 실행한 후, 아래 코드를 한 줄씩 입력하여 실행해보세요. 각 명령어 실행 결과를 확인하고, 실행 화면을 캡처하여 제출해주세요.
```
```python
a = 5
a

import numpy as np
data = [np.random.standard_normal() for i in range(7)]
data
```
<img width="681" height="516" alt="image" src="https://github.com/user-attachments/assets/29e7c2b0-aec2-44b7-941d-ace53d9e0b51" />
-->

### 주피터 노트북 실행하기 

```
주피터 노트북을 실행한 후, 새로운 노트북을 생성하세요.
코드 셀에 print("Hello, World!")를 입력하고 실행한 뒤, 출력 결과가 나타난 화면을 캡처하여 제출해주세요.
```

<img width="1455" height="550" alt="image" src="https://github.com/user-attachments/assets/6d8a99e6-62cf-4d8d-bbf7-3ee2fe31bc39" />


## 파이썬 기초  
# 🐍 파이썬 기초 핵심 정리 (Python Basics)

파이썬의 기본적인 문법, 객체 모델, 그리고 제어 흐름에 대한 핵심 내용을 정리한 문서입니다.

---

## 1. 파이썬 시맨틱 (Semantics)

### 🔹 들여쓰기 (Indentation)
* **공백 기반 구조:** 파이썬은 중괄호 `{}` 대신 **공백(스페이스 4칸)**을 사용하여 코드를 구조화합니다.
* **가독성:** 들여쓰기는 단순한 규칙이 아니라 파이썬의 정체성이며, 코드의 가독성을 높여줍니다.

### 🔹 모든 것은 객체 (Everything is an object)
* 모든 숫자, 문자열, 함수, 클래스 등은 파이썬 인터프리터에서 **객체(Object)**라는 상자 안에 저장됩니다.
* 각 객체는 고유한 **자료형(Type)**과 **데이터**를 가집니다.

### 🔹 변수와 참조 (References)
* 변수에 값을 대입하면 객체의 복사본이 아닌, 해당 객체에 대한 **참조(Reference)**가 생성됩니다.
* `a = b`와 같이 대입하면 두 변수는 실제로 **동일한 객체**를 가리키게 됩니다.

---

## 2. 타입 시스템 (Type System)

### 🔹 동적 참조와 강한 타입
* **동적 참조:** 변수 자체에는 고유한 타입이 없으며, 할당을 통해 다른 타입의 객체를 자유롭게 참조할 수 있습니다.
* **강한 타입:** 파이썬은 묵시적인 형 변환을 허용하지 않습니다. (예: `'5' + 5` 실행 시 `TypeError` 발생)

### 🔹 덕 타이핑 (Duck Typing)
* 객체의 실제 자료형보다 **그 객체가 어떤 메서드나 행동을 지원하는지**가 더 중요합니다.
* "만약 어떤 새가 오리처럼 걷고 오리처럼 팩팩 운다면 그것은 오리다."

```python
# 객체가 순회 가능한지(Iterable) 확인하는 함수
def isiterable(obj):
    try:
        iter(obj)
        return True
    except TypeError:
        return False
```

---

## 3. 주요 연산자 및 모듈

### 🔹 이항 연산자 요약

| 연산자 | 설명 | 연산자 | 설명 |
| :--- | :--- | :--- | :--- |
| `a + b` | 더하기 | `a // b` | 나눗셈의 몫 (소수점 버림) |
| `a - b` | 빼기 | `a ** b` | a의 b승 (거듭제곱) |
| `a * b` | 곱하기 | `a == b` | 값이 같은지 비교 |
| `a / b` | 나누기 | `a is b` | 동일 객체 참조 여부 확인 |

### 🔹 모듈 임포트 (Import)

```python
import some_module as sm             # 모듈 별칭 지정
from some_module import PI as pi, g  # 특정 변수/함수만 호출
```

---

## 4. 스칼라 자료형 (Scalar Types)

* **None:** 파이썬의 `null` 값 (유일한 인스턴스)
* **str:** 문자열 자료형 (유니코드 UTF-8 인코딩)
* **float/int:** 64비트 부동소수점수 및 임의 정밀도 정수
* **bool:** `True` 또는 `False`
* **datetime:** 날짜와 시간 정보 처리 (`datetime` 모듈 사용)

### 🔹 문자열 포매팅 (f-string)

```python
amount = 10
currency = "Pesos"
# 문자열 앞에 f를 붙여 중괄호 안에 표현식을 직접 삽입
result = f"{amount} {currency} is worth US${amount / 88.46:.2f}"
```

---

## 5. 제어 흐름 (Control Flow)

### 🔹 if, elif, else
조건에 따라 코드 블록의 실행 여부를 결정합니다.

### 🔹 for 문
리스트, 튜플, range 등 컬렉션이나 이터레이터를 순회합니다.
* `continue`: 남은 블록을 건너뛰고 다음 순회로 이동
* `break`: 반복문을 즉시 종료

### 🔹 range 함수
균일한 간격의 연속된 정수 이터레이터를 반환합니다.
```python
list(range(10))        # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
list(range(0, 20, 2))  # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

### 🔹 pass
아무런 작업도 하지 않음을 나타내며, 나중에 구현할 코드를 위한 플레이스홀더로 사용합니다.

---


---

# 2️⃣ 실습 과제

**주피터 노트북에서 아래의 코드 셀을 실행하고, 출력 결과를 캡처하여 제출하세요.**

```python
key = 7
data = [44059, 44050, 39, 52626, 54623, 38]

print("".join(chr(x ^ key) for x in data))
```

<img width="1471" height="670" alt="image" src="https://github.com/user-attachments/assets/c656f48f-f94e-4538-997d-d8d2caf34bfd" />


### 🎉 수고하셨습니다.






