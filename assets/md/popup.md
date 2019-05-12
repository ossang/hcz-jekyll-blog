# Component
---
```typescript
export class PopupSampleComponent implements OnInit {

  isShowPopup : boolean;
  header:string;
  width:number;

  constructor() { }

  ngOnInit() {
    this.header = '데모 팝업!';
    this.width = 800;
  }

  showPopup(){
    this.isShowPopup = true;
  }

  hideEvent(event){
    this.isShowPopup = false;
  }
}
```

# Html
---
```html
<button type="button" (click)="showPopup()">팝업 열기</button>

<olib-popup [header]="header" [isShowPopup]="isShowPopup" [width]="width" (hideEvent)="hideEvent($event)" >
sample data contents!!
</olib-popup>
```