# Component
---
```typescript
export class RadioSampleComponent implements OnInit {

  sampleConfig : OlibRadioConfig;

  constructor() { }

  ngOnInit() {
    this.sampleConfig = new OlibRadioConfig("sample","all");
    this.sampleConfig.addOption('test all','all');
    this.sampleConfig.addOption('test 1','1');
    this.sampleConfig.addOption('test 2','2');
    this.sampleConfig.addOptionDisable('test 3','3','true');
  }

}
```

# Html
---
```html
<olib-radio [config]="sampleConfig"></olib-radio>
```