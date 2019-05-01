
# Methods

|Name| Description|
|---|---|
|initializeCols()|테이블 컬럼 초기 설정|
|initializeDatas()|테이블 데이터 초기 설정|
|initializeOptions()|테이블 옵션 초기 설정|

<br>

---
# OlibTableColsModel
| Name | Type | Description |
|---|---|---|
|field|string|데이터 필드명|
|header|string|칼럼명|
|width|string|칼럼 너비(%)|
|isFilter|boolean|칼럼 필터 사용 유무|
|isSort|boolean|칼럼 정렬아이콘 표시 유무|
|isDate|boolean|데이트 타입 칼럼 유무|

<br>

---

# OlibTableOptionModel
| Name  | Type | Default | Description
|---|---|---|---|
| isCheckbox  | boolean  | false  | 체크박스 사용 유무 |
| isFilter  | boolean  | false  | 테이블컬럼 필터 기능 사용 유무 |
| isSort  | boolean  | false  | 테이블컬럼 정렬 기능 사용 유무 |
| isPaginator  | boolean  | true  | 페이징 사용 유무 |
| isExport  | boolean  | false  | csv 데이터 내보내기 기능 사용 유무 |
| rowsPerPage  | array  | [10,20,30]  | 표시 할 데이터 크기 선택 옵션 |
| isCustom  | boolean  | false  | 커스텀 컬럼 설정 사용 유무 |