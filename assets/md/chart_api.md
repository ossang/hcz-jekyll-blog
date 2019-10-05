# OlibChartPieConfig
| Name | Type | Description |
|---|---|---|
|title|string|제목 |
|data|any| {value : '값' , name : '표시명'}|


# OlibChartBarConfig
| Name | Type | Description |
|---|---|---|
|isVertical|boolean|세로 표시 여부(true : 세로바 표시 , false : 가로바 표시) |
|categorys|any|카테코리명 배열 예) ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']|
|values|any|카테고리 인덱스에 해당하는 값 예) [111, 222, 333, 444, 555, 666, 777]|


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
