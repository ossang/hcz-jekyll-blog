# Component
---
```typescript
export class CheckboxSampleComponent implements OnInit {

  sampleConfig : OlibCheckConfig;

  constructor() { }

  ngOnInit() {
    this.sampleConfig = new OlibCheckConfig();
    this.sampleConfig.$allSelectedLabel = "전체선택";
    this.sampleConfig.$isVertical = false;

    let checkboxList = new Array;
    checkboxList.push(new OlibCheckbox(1,"test1"));
    checkboxList.push(new OlibCheckbox(2,"test2"));
    checkboxList.push(new OlibCheckbox(3,"test3"));
    this.sampleConfig.$checkboxList = checkboxList;
  }
}
```

# Html
---
```html
<olib-checkbox [config]="sampleConfig"></olib-checkbox>
```