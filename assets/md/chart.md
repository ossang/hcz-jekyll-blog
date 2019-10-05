# PIE Chart
---
```typescript
export class ChartPieSampleComponent {

  pieChartConfig : OlibChartPieConfig;

  options: any = {};
  themeSubscription: any;

  constructor() {
    this.pieChartConfig = new OlibChartPieConfig;
    this.pieChartConfig.$title = "sample";
    this.pieChartConfig.$data = [
      { value: 111, name: 'Aaa' },
      { value: 222, name: 'Bbb' },
      { value: 333, name: 'Ccc' },
      { value: 444, name: 'Ddd' },
      { value: 555, name: 'Eee' },
    ];
  }
}
```
<br>

```html
<olib-chart-pie [config]="pieChartConfig"></olib-chart-pie>
```

<br><br><br>

# BAR Chart
---
```typescript
export class ChartBarSampleComponent {

  barChartConfig : OlibChartBarConfig;
  
  constructor() { 
    this.barChartConfig = new OlibChartBarConfig;
    this.barChartConfig.$isVertical = true;
    this.barChartConfig.$categorys = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'];
    this.barChartConfig.$values = [111, 222, 333, 444, 555, 666, 777];
  }
}
```
<br>  

```html
<olib-chart-bar [config]="barChartConfig"></olib-chart-bar>
```

<br><br><br>

# LINE Chart
---
```typescript
export class ChartLineSampleComponent {

  lineChartConfig : OlibChartLineConfig;

  constructor() { 
    this.lineChartConfig = new OlibChartLineConfig;
    this.lineChartConfig.$categorys = ['1', '2', '3', '4', '5', '6', '7', '8', '9'];

    let datas = [];
    datas.push(new OlibChartLineData('line 1',[1, 3, 9, 27, 81, 247, 741, 2223, 6669]));
    datas.push(new OlibChartLineData('line 2',[1, 2, 4, 8, 16, 32, 64, 128, 256]));
    datas.push(new OlibChartLineData('line 3',[1 / 2, 1 / 4, 1 / 8, 1 / 16, 1 / 32, 1 / 64, 1 / 128, 1 / 256, 1 / 512]));
    this.lineChartConfig.$datas = datas;
  }
}
```
<br>  

```html
<olib-chart-line [config]="lineChartConfig"></olib-chart-line>
```

<br><br><br>