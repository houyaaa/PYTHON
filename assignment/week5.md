# Python 5주차 정규 과제 

📌Python 정규과제는 매주 정해진 분량의 『*파이썬 라이브러리를 활용한 데이터 분석*』 을 읽고 학습하는 것입니다. 이번주는 아래의 **Python_5th_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 참고 자료를 통해 보완하는 것이 좋습니다.

**교재 실습 예제 파일은 07_Python_Template 레포지토리의 notebooks 폴더에 업로드되어 있습니다.**

**아나콘다 환경에서는 많은 패키지가 기본적으로 포함되어 있어 별도의 설치 없이 사용할 수 있지만, 환경에 따라 conda install이나 pip install이 필요할 수 있습니다.**

**👀(수행 인증샷은 필수입니다.)** 

## Python_5th_TIL

### 6장 데이터 로딩과 저장, 파일 형식
#### 1. 텍스트 파일에서 데이터를 읽고 쓰는 법
#### 2. 이진 데이터 형식
#### 3. 웹 API와 함께 사용하기
#### 4. 데이터베이스와 함께 사용하기
#### 5. 마치며
### 7장 데이터 정제 및 준비
#### 1. 누락된 데이터 처리하기
#### 2. 데이터 변형 


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.25~82    | ✅         |
| 2주차 | p.83~129   | ✅         |
| 3주차 | p.131~179  | ✅         |
| 4주차 | p.181~246 | ✅         |
| 5주차 | p.247~309 | ✅         |
| 6주차 | p.310~379 | 🍽️         |
| 7주차 | p.381~465 | 🍽️         |


<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 학습 내용 정리

## 1. 텍스트 파일에서 데이터를 읽고 쓰는 법

### 개념정리
* 판다스는 `read_csv`, `read_table` 등 표 형식의 자료를 데이터프레임으로 읽어오는 다양한 함수를 제공
* `read_csv`는 쉼표(,)를 기본 구분자로 사용하며 가장 빈번하게 활용
* 주요 옵션으로 `header`는 열 이름 행 번호 지정, `names`는 직접 열 이름 리스트 전달, `index_col`은 색인으로 사용할 열 지정 등이 있음
* `skiprows`로 특정 행을 제외하거나 `na_values`로 누락된 값을 처리할 문자열 목록 지정 가능
* 대용량 파일은 `nrows`로 일부만 읽거나 `chunksize` 옵션을 통해 특정 행 개수 단위로 나누어 순회하며 읽기 가능
* 데이터 기록 시에는 `to_csv` 메서드를 사용하며 구분자(`sep`), 색인 포함 여부(`index`), 헤더 포함 여부(`header`) 등을 설정
<br>

### 실습 인증

<img width="716" height="686" alt="image" src="https://github.com/user-attachments/assets/dca86fb6-282f-4100-8844-1555a2063b36" />
<img width="776" height="697" alt="image" src="https://github.com/user-attachments/assets/f7a184b2-e18a-4e65-bc75-a081cc888d3c" />
<img width="600" height="561" alt="image" src="https://github.com/user-attachments/assets/a14dcc53-1277-4e9d-8520-ed0ed976dd45" />


## 2. 이진 데이터 형식

### 개념정리
* **Pickle**: 파이썬 내장 `pickle` 모듈을 이용해 객체를 직렬화하며 `to_pickle`로 저장하고 `read_pickle`로 불러옴
* **Excel**: `ExcelFile` 클래스나 `read_excel` 함수를 통해 시트 데이터를 읽고, `to_excel` 메서드로 저장
* **HDF5**: 대량의 과학 계산용 배열 데이터를 저장하기 위한 계층적 포맷으로 `HDFStore`를 통해 딕셔너리처럼 객체 저장 및 쿼리 연산 지원
* **Parquet**: 분산 저장소용으로 설계된 이진 형식이며 `read_parquet` 함수로 읽기 가능

<br>

### 실습 인증

<img width="917" height="693" alt="image" src="https://github.com/user-attachments/assets/6892b2b1-5ab7-415a-af19-d40bb84ac537" />
<img width="886" height="707" alt="image" src="https://github.com/user-attachments/assets/467a1c19-20da-4423-b95a-0169e9938414" />


## 3. 웹 API와 함께 사용하기

### 개념정리
* `requests` 패키지를 이용해 HTTP GET 요청을 보내고 외부 API 데이터를 가져옴
* 응답 객체의 `json` 메서드로 JSON 내용을 파이썬 딕셔너리 형태로 변환함
* 변환된 데이터를 `pd.DataFrame` 생성자에 전달하고 관심 있는 필드(열)만 추출하여 구성함

<br>

### 실습 인증
<img width="828" height="700" alt="image" src="https://github.com/user-attachments/assets/bdaeb153-5526-40f0-b46b-ed9f539905a3" />
<img width="798" height="636" alt="image" src="https://github.com/user-attachments/assets/3e64737c-8dc8-4f26-96c9-029a6566f7ea" />

<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->


## 4. 데이터베이스와 함께 사용하기

### 개념정리
* 파이썬 내장 `sqlite3`나 `SQLAlchemy`를 통해 관계형 데이터베이스와 연결함
* 쿼리 실행 후 반환된 튜플 리스트를 데이터프레임으로 변환할 때 열 이름을 지정해줘야 함
* `read_sql` 함수를 사용하면 SQL 쿼리 결과를 별도 절차 없이 바로 데이터프레임 형식으로 읽어옴

<br>

### 실습 인증

<img width="920" height="677" alt="image" src="https://github.com/user-attachments/assets/f1e27df5-ab0b-4b74-aaba-539e7da2066a" />
<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->


## 5. 누락된 데이터 처리하기

### 개념정리

* 판다스는 누락된 데이터를 `NaN`(실수형)이나 `None`(객체형)으로 표시하며 통계 계산 시 기본적으로 배제
* `isna`로 결측 여부를 확인하고 `dropna`로 결측치가 포함된 행/열을 제거하며 `fillna`로 특정 값이나 보간법으로 채움
* 넘파이 기반 방식의 한계를 극복하기 위해 `Int64`, `boolean`, `string` 등 확장 데이터 유형을 도입하여 결측치를 `<NA>`로 일관되게 표현
* 확장 유형은 `astype` 메서드를 통해 기존 데이터프레임의 열에 쉽게 적용 가능

<br>

### 실습 인증
<img width="818" height="715" alt="image" src="https://github.com/user-attachments/assets/fb306604-90db-4b81-bb15-a56ba3e5c354" />
<img width="927" height="680" alt="image" src="https://github.com/user-attachments/assets/0040245a-8497-4b70-9ec0-281070a3c11e" />
<img width="829" height="617" alt="image" src="https://github.com/user-attachments/assets/9349771f-b3ef-4cd3-9d6c-76956d3f6ec0" />

<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->


## 6. 데이터 변형 

### 개념정리

* **중복 제거**: `duplicated`로 중복 행을 탐색하고 `drop_duplicates`로 필터링함. `keep='last'` 옵션으로 마지막 값을 유지 가능
* **매핑 및 치환**: `map`으로 요소별 변형을 수행하고 `replace`로 특정 값을 치환하며 `rename`으로 축 색인 이름을 바꿈
* **이산화**: `cut`으로 데이터를 특정 경계값 기준으로 나누거나 `qcut`을 이용해 표본 사분위수 기반의 균등한 그룹으로 분할
* **계층적 색인**: `MultiIndex`를 통해 축에 둘 이상의 단계를 지정하여 고차원 데이터를 다룸
* **병합**: `merge`는 키 기준 SQL 조인을 수행하고 `concat`은 축을 따라 데이터를 이어 붙임
* **재구성**: `stack`은 열을 행으로, `unstack`은 행을 열로 피벗하며 `melt`는 넓은 형식을 긴 형식으로 변형

<br>

### 실습 인증
<img width="916" height="769" alt="image" src="https://github.com/user-attachments/assets/ccc157bd-0440-43cd-a481-14085273653d" />
<img width="922" height="711" alt="image" src="https://github.com/user-attachments/assets/34c262dd-7027-40a0-8cfb-fce69237014f" />

<!-- 예제 실습을 진행한 후, 실행 화면을 2-3장 캡쳐하여 제출해주세요. -->

<!-- 이 부분을 지우고 실행 화면을 제출해주세요. -->



# 2️⃣ 실습 과제

각 문제에 대한 실행 결과가 확인되도록 코드를 작성하고 실행한 뒤, **모든 문제의 실행 화면을 캡처하여 제출하시기 바랍니다.**

**1. 아래 코드를 실행하여 텍스트와 데이터를 선언합니다.**
```python
import pandas as pd
import json
import requests

# 1. 테스트용 CSV 내용 (메모리 내 시뮬레이션용)
csv_data = "id,name,score,note\n1,Kim,85,NA\n2,Lee,NULL,Good\n3,Park,90,None"
with open("test_data.csv", "w") as f:
    f.write(csv_data)

# 2. 테스트용 JSON 문자열
json_obj = """
{
    "company": "DataService",
    "employees": [
        {"name": "Alice", "age": 30, "dept": "IT"},
        {"name": "Bob", "age": 25, "dept": "HR"}
    ]
}
"""
```

**2. 문제**
```
1. CSV 파일 읽기 및 결측치 지정
  - 문제 설명: 제공받은 test_data.csv 파일을 읽어오기(단, 데이터의 특성에 맞게 옵션 설정)
  - read_csv()를 사용하여 파일을 읽으세요.
  - 이때 NA, NULL, None이라는 문자열을 모두 **결측치(NaN)**로 인식하도록 na_values 옵션을 설정하세요.
  - print()를 이용해 읽어온 DataFrame을 출력하세요.

2. JSON 데이터 변환 및 특정 데이터 추출
  - 문제 설명: 문자열 형태의 JSON 데이터를 파싱하여 직원 명단만 추출
  - json.loads()를 사용하여 json_obj 문자열을 파이썬 객체로 변환하세요.
  - 변환된 객체에서 employees 리스트만 추출하여 DataFrame으로 만드세요.
  - print()를 이용해 생성된 직원 명단 DataFrame을 출력하세요.

3. 웹 API 데이터 가져오기
  - 문제 설명: 판다스 깃허브 저장소의 이슈(Issues) 데이터를 가져와 상위 항목 확인
  - requests.get()을 사용하여 https://api.github.com/repos/pandas-dev/pandas/issues URL의 데이터를 가져오세요.
  - 응답받은 JSON 데이터를 DataFrame으로 변환하세요.
  - print()를 이용해 데이터의 상단 5행(head)을 출력하세요.
```

<!-- 이 부분을 지우고 인증 사진을 제출해주세요.-->

#1 
<img width="720" height="287" alt="image" src="https://github.com/user-attachments/assets/ecc930e7-7f4f-4695-9ed9-20e0ccb1313b" />

#2
<img width="533" height="379" alt="image" src="https://github.com/user-attachments/assets/93bf3091-caca-49e2-8399-828475026685" />

#3
<img width="644" height="702" alt="image" src="https://github.com/user-attachments/assets/c9c8d0aa-ccc2-4152-a3c5-c96cbaf348b3" />



### 🎉 수고하셨습니다.






