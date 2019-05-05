# Component
---
```typescript
export class DatepickerSampleComponent implements OnInit {

  selectedDate : Date[];
  
  constructor() { }

  ngOnInit() {
  }

  rangeDates(data){
    this.selectedDate = data;
  }

}

```
# Html
---
```html
<olib-datepicker (rangeDates)="rangeDates($event)" showTime="false" mode="single" ></olib-datepicker>
```

