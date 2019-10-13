# PIE Chart (STATIC)
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

# PIE Chart (DYNAMIC)
---
```typescript
export class ChartPieSample2Component {

  dynamicPieChartConfig : OlibChartPieConfig;

  constructor() {
    this.dynamicPieChartConfig = new OlibChartPieConfig;
    this.dynamicPieChartConfig.$title = "dynamic";
    this.dynamicPieChartConfig.$isDynamicData = true;
    this.dynamicPieChartConfig.$updateTime = 5000;
    this.ramdomData();

    setInterval(()=>{
      this.ramdomData();
    },this.dynamicPieChartConfig.$updateTime);
  }

  ramdomData(){
    let datas = [];
    let cnt = Math.round((Math.random() % 10) * 10);
    for(let i =0; i<cnt; i++){
      datas[i] = {name:"label - "+i,value:Math.random()*1000}
    }
    this.dynamicPieChartConfig.$data = datas;
  }
}
```

<br>

```html
<olib-chart-pie [config]="pieChartConfig"></olib-chart-pie>
```

<br><br><br>

# BAR Chart (STATIC)
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

# BAR Chart (DYNAMIC)
---
```typescript
export class ChartBarSample2Component {

  dynamicBarChartConfig : OlibChartBarConfig;

  constructor() { 
    this.dynamicBarChartConfig = new OlibChartBarConfig;
    this.dynamicBarChartConfig.$isVertical = false;
    this.dynamicBarChartConfig.$isDynamicData = true;
    this.dynamicBarChartConfig.$updateTime = 5000;

    this.ramdomData();

    setInterval(()=>{
      this.ramdomData();
    },this.dynamicBarChartConfig.$updateTime);
  }

  ramdomData(){
    let categorys = [];
    let values = [];
    for(let i =0; i<10; i++){
      categorys[i]="category "+i;
      values[i]=Math.random()*1000;
    }
    this.dynamicBarChartConfig.$categorys = categorys;
    this.dynamicBarChartConfig.$values = values;
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

# TEXT
---
```typescript
export class ChartTextSampleComponent implements OnInit {

  @Input("status")
  status : any;

  config : OlibChartTextConfig;

  constructor() { }

  ngOnInit() {
    this.config = new OlibChartTextConfig;
    this.config.$status = this.status;
    this.config.$title = "sample title";
    this.config.$value = 99999;
  }
}
```
<br>

```html
<olib-chart-text [config]="config"></olib-chart-text>
```