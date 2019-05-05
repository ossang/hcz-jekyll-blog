# Methods
| Name | Param | Description |
|---|---|---|
|addOption|label,value| 'label' : 표시 라벨, 'value' : 데이터 |
|addOptionDisable|label,value,disabled|'label' : 표시 라벨, 'value' : 데이터 , 'disabled' : 'ture : 비활성', 'false : 활성' |
<br>

# Constructor Example
```typescript
let sampleConfig = new OlibRadioConfig("그룹명","기본값");
sampleConfig.addOption('라벨명','기본값');
sampleConfig.addOption('라벨명2','데이터');
```