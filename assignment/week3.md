# Python 3주차 정규 과제 

📌Python 정규과제는 매주 정해진 분량의 『*파이썬 라이브러리를 활용한 데이터 분석*』 을 읽고 학습하는 것입니다. 이번주는 아래의 **Python_3rd_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 참고 자료를 통해 보완하는 것이 좋습니다.

**교재 실습 예제 파일은 07_Python_Template 레포지토리의 notebooks 폴더에 업로드되어 있습니다.**

**👀(수행 인증샷은 필수입니다.)** 

## Python_3rd_TIL

### 4장 넘파이 기본: 배열과 벡터 연산
#### 1. 다차원 배열 객체 ndarray
#### 2. 난수 생성
#### 3. 유니버설 함수: 배열의 각 원소를 빠르게 처리하는 함수
#### 4. 배열을 이용한 배열 기반 프로그래밍
#### 5. 배열 데이터의 파일 입출력
#### 6. 선형대수
#### 7. 계단 오르내리기 예제
#### 8. 마치며 


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.25~82    | ✅         |
| 2주차 | p.83~129   | ✅         |
| 3주차 | p.131~179  | ✅         |
| 4주차 | p.181~246 | 🍽️         |
| 5주차 | p.247~309 | 🍽️         |
| 6주차 | p.310~379 | 🍽️         |
| 7주차 | p.381~465 | 🍽️         |


<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 학습 내용 정리

## 1. 다차원 배열 객체 ndarray

### 개념정리
<br>

**NumPy**

- NumPy = Numerical Python
- 산술계산을 위한 필수 패키지
- 핵심 자료구조 **ndarray**: 동일한 자료형의 데이터를 다차원 배열 형태로 저장
- 리스트와 달리 ndarray는 **벡터화 연산**을 지원, 반복문 없이 빠르게 계산 가능
- ndarray는 배열의 **크기(shape)**, **차원(ndim)**, **자료형(dtype)** 등의 속성을 가짐
- `array()`를 사용하면 리스트나 튜플로부터 배열 생성 가능
- `zeros()`, `ones()`, `arange()` -> 원하는 형태의 배열을 쉽게 만들 수 있음
- 슬라이싱, 인덱싱을 통해 배열의 일부를 선택가능
- 다차원 배열에서는 행과 열을 함께 지정 가능
<br>
<br>
<br>

### 실습 인증

<img width="518" height="721" alt="image" src="https://github.com/user-attachments/assets/c3726faa-e4a8-4b98-9108-a6be9ae79ae6" />
<img width="481" height="726" alt="image" src="https://github.com/user-attachments/assets/e04f712d-417d-4114-b64a-91e89ccf5214" />

<br>
<br>
<br>
<br>


## 2. 난수 생성

### 개념정리
- NumPy는 `random` 모듈을 통해 다양한 형태의 난수를 생성

- `rand()` : 0과 1 사이의 균등분포 난수를 생성

- `randn()` : 평균 0, 표준편차 1인 표준정규분포 난수를 생성

- `randint()` : 지정한 범위 내의 정수 난수를 생성

- `seed()`를 사용하면 난수 생성 결과를 고정할 수 있어, 같은 코드를 실행했을 때 항상 같은 결과를 얻을 수 있음
- 난수 생성은 데이터 샘플링, 시뮬레이션, 머신러닝 실험, 랜덤 테스트 데이터 생성 등에 자주 사용

<br>
<br>
<br>
<br>



### 실습 인증
<img width="517" height="719" alt="image" src="https://github.com/user-attachments/assets/8923d29b-7a51-4460-b691-6ce2e29966e8" />
<img width="523" height="721" alt="image" src="https://github.com/user-attachments/assets/92fe100f-8048-4193-9cfb-b20d1eac1d84" />


<br>
<br>
<br>
<br>



## 3. 유니버설 함수: 배열의 각 원소를 빠르게 처리하는 함수

### 개념정리

- 유니버설 함수(ufunc)는 배열의 각 원소에 대해 빠르게 반복 연산을 수행하는 함수
- 반복문 없이 배열 전체에 연산을 적용할 수 있어 매우 효율적
- 대표적인 유니버설 함수 -> sqrt(), exp(), add(), maximum()
- 유니버설 함수는 단항 함수와 이항 함수
  - 단항 함수: 원소 하나씩 처리 (sqrt, abs, exp)
  - 이항 함수: 두 배열의 원소끼리 계산 (add, maximum)

- NumPy의 유니버설 함수는 배열 기반 계산의 핵심 도구

<br>
<br>
<br>
<br>
<br>
<br>

### 실습 인증

<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->
<img width="476" height="723" alt="image" src="https://github.com/user-attachments/assets/2bdbad6b-2c9e-46f2-910c-ee3038595331" />
<img width="492" height="648" alt="image" src="https://github.com/user-attachments/assets/0b6eddfd-3eaa-4d4f-9857-8b6197bbfe44" />

<br>
<br>
<br>
<br>
<br>
<br>

## 4. 배열을 이용한 배열 기반 프로그래밍

### 개념정리
- 배열 기반 프로그래밍은 반복문 대신 배열 연산을 활용하여 데이터를 처리하는 방식
- NumPy에서는 배열끼리의 사칙연산이 원소별로 자동 수행(**벡터화(vectorization)**) -> 파이썬 기본 반복문보다 훨씬 빠름
- 브로드캐스팅을 통해 크기가 다른 배열도 조건에 맞으면 자동으로 형태를 맞춰 계산할 수 있음
- 조건문도 배열 전체에 적용할 수 있어 데이터 분석에서 매우 유용
- 이러한 방식은 코드가 짧고 가독성이 높으며, 연산 속도도 빠르다는 장점

<br>
<br>
<br>
<br>
<br>
<br>

### 실습 인증

<img width="530" height="733" alt="image" src="https://github.com/user-attachments/assets/4d0fc7f3-babe-4015-a24b-fec6b2efa53d" />
<img width="544" height="699" alt="image" src="https://github.com/user-attachments/assets/23f4fe81-fb6f-44ad-b101-f70b17dd26d1" />


<br>
<br>
<br>
<br>
<br>
<br>
## 5. 배열 데이터의 파일 입출력

### 개념정리

- NumPy는 배열 데이터를 파일로 저장하거나 다시 불러올 수 있는 기능을 제공
- `save()`: 배열을 .npy 형식으로 저장
- `load()`: 저장된 배열을 불러옴
- `savez()`: 여러 배열을 한 파일에 저장
- 텍스트 파일 형식으로 저장할 때는 `savetxt()`와 `loadtxt()`


<br>
<br>
<br>
<br>
<br>
<br>

### 실습 인증
<img width="476" height="745" alt="image" src="https://github.com/user-attachments/assets/31e20462-7271-419a-a2f7-fa57bdaf6ff4" />

<img width="483" height="666" alt="image" src="https://github.com/user-attachments/assets/ac86afd6-28dd-4213-9852-280923676e22" />

<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->
<br>
<br>
<br>
<br>
<br>
<br>

## 6. 선형대수

### 개념정리
- NumPy는 선형대수 계산을 위한 다양한 기능을 제공하며, numpy.linalg 모듈을 사용
- 행렬의 곱셈, 전치행렬, 역행렬, 행렬식 등을 계산
- 선형대수는 데이터 분석, 회귀분석, 최적화, 머신러닝 등에서 핵심적으로 사용
- `dot()` 또는 @ 연산자를 사용하여 행렬 곱을 수행
- `inv()` 역행렬
- `det()` 행렬식
- `eig()` 고유값과 고유벡터

<!-- 이 부분을 지우고 새롭게 배우게 된 내용을 정리해주세요. -->
<br>
<br>
<br>
<br>
<br>
<br>

### 실습 인증
<img width="357" height="710" alt="image" src="https://github.com/user-attachments/assets/e99ba67b-56c8-49b1-bcbc-2e2ca06579b9" />
<img width="342" height="720" alt="image" src="https://github.com/user-attachments/assets/31700a3e-eb54-4c8c-a3b9-bb4e5368323d" />


<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->

<br>
<br>
<br>
<br>
<br>
<br>

## 7. 계단 오르내리기 예제

### 개념정리
- 랜덤 워크(random walk) 시뮬레이션의 대표적인 예
- 각 단계에서 위로 1칸 올라가거나 아래로 1칸 내려가는 과정을 반복하여 경로를 만듦
- NumPy를 사용하면 반복적인 이동 과정을 배열 연산으로 빠르게 계산 가능
- `random.randint()` 또는 `random.choice()`: 이동 방향
- `cumsum()`: 누적합


<!-- 이 부분을 지우고 새롭게 배우게 된 내용을 정리해주세요. -->
<br>
<br>
<br>
<br>
<br>
<br>

### 실습 인증
<img width="387" height="661" alt="image" src="https://github.com/user-attachments/assets/588c8963-ec19-442c-95e8-6eb7ce70fa6d" />
<img width="844" height="470" alt="image" src="https://github.com/user-attachments/assets/840a9955-24ab-4778-af0d-dd43cf7b51c6" />


<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->

<br>
<br>
<br>
<br>
<br>
<br>

# 2️⃣ 실습 과제

각 문제에 대한 실행 결과가 확인되도록 코드를 작성하고 실행한 뒤, **모든 문제의 실행 화면을 캡처하여 제출하시기 바랍니다.**

**1. 아래 코드를 실행하여 5일간 3개 품목의 판매량 데이터를 생성합니다.**
```python
import numpy as np

# 5일간 3개 품목의 판매량
# 행: 월, 화, 수, 목, 금 / 열: 사과, 배, 포도
sales = np.array([
    [45, 30, 75],  # 월요일
    [50, 60, 15],  # 화요일
    [85, 20, 40],  # 수요일
    [30, 90, 55],  # 목요일
    [70, 45, 80]   # 금요일
])
```

**2. 문제**
```
1. 품목별 총 판매량 계산 및 출력
  - 문제 설명: 각 품목이 5일 동안 총 몇 개 팔렸는지 계산
  - sum() 메서드의 axis 옵션을 활용하여 품목별 합계를 구하세요.
  - print()를 이용해 품목별 총 판매량 리스트를 출력하세요.

2. 특정 기간 및 품목 추출
  - 문제 설명: 수요일부터 금요일까지(3~5행), 첫 번째와 두 번째 품목(사과, 배)의 판매량만 따로 보기 
  - 배열 슬라이싱을 사용하여 해당 데이터를 추출하세요.
  - print()를 이용해 추출된 3x2 배열을 출력하세요.

3. 목표 미달 판매량 조정
  - 문제 설명: 하루 판매량이 40개 미만인 경우, 값을 0으로 표시하고, 40개 이상인 경우는 기존 값을 유지
  - np.where() 함수를 사용하여 40 미만은 0, 40 이상은 원래 값을 가지는 새로운 배열을 만드세요.
  - print()를 이용해 수정된 배열을 출력하세요.
```

<!-- 이 부분을 지우고 인증 사진을 제출해주세요.-->

## 1.
<img width="282" height="148" alt="image" src="https://github.com/user-attachments/assets/a3ba9551-5425-47f4-a1fc-51a3583fc7b3" />


## 2. 
<img width="225" height="139" alt="image" src="https://github.com/user-attachments/assets/020fddce-f102-4200-aeaf-1be448af22c2" />


## 3.

<img width="305" height="205" alt="image" src="https://github.com/user-attachments/assets/428737e7-dc33-4a04-8368-00722dbd7a66" />

### 🎉 수고하셨습니다.






