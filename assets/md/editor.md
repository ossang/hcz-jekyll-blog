# Component
---
```typescript
export class EditorSampleComponent implements OnInit {

  data : any;
  
  constructor() { }

  ngOnInit() {
    this.data = 'sample data!!';
  }
}
```

# Html
---
```html
<olib-editor [body]="data"></olib-editor>
```