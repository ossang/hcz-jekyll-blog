# OlibChartPieConfig
| Name | Type | Description |
|---|---|---|
|title|string|제목 |
|data|any| {value : '값' , name : '표시명'}|
|isDynamicData|boolean| true:데이터 업데이트사용 , false:정적데이터 사용|
|updateTime|number| 데이터 업데이트 주기 (1000 -> 1초)|
|isLoading|boolean| 차트 로딩 표시 여부(true:표시, false:표시안함)|

# OlibChartBarConfig
| Name | Type | Description |
|---|---|---|
|isVertical|boolean|세로 표시 여부(true : 세로바 표시 , false : 가로바 표시) |
|categorys|any|카테코리명 배열 예) ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']|
|values|any|카테고리 인덱스에 해당하는 값 예) [111, 222, 333, 444, 555, 666, 777]|
|isDynamicData|boolean| true:데이터 업데이트사용 , false:정적데이터 사용|
|updateTime|number| 데이터 업데이트 주기 (1000 -> 1초)|
|isLoading|boolean| 차트 로딩 표시 여부(true:표시, false:표시안함)|

# OlibChartLineConfig
| Name | Type | Description |
|---|---|---|
|categorys|any|카테고리명 배열 예)['1', '2', '3', '4', '5', '6', '7', '8', '9'] |
|datas|OlibChartLineData[]| 라인별 옵션 배열|

# OlibChartLineData
| Name | Type | Description |
|---|---|---|
|name|string|라인별 타이틀 |
|type|string|차트 타입 (값 'line' 고정) |
|data|any| 카테고리 인덱스에 해당하는 배열 값 예)[1, 3, 9, 27, 81, 247, 741, 2223, 6669]|

# OlibChartTextConfig
| Name | Type | Description |
|---|---|---|
|title|any| 타이틀 명 |
|status|string|info, primary, danger, warning|
|value|any| 표시 값|