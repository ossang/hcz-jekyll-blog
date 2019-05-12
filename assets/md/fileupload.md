# Component
---
```typescript
export class FileuploadSampleComponent implements OnInit {

  @ViewChild('olibfile') 
  olibfile: FileUpload;

  config : OlibFileuploadConfig;
  file : OlibFileupload;

  constructor() { }

  ngOnInit() {
    this.config = new OlibFileuploadConfig;
    this.config.$accept='image/*';
    this.config.$authToken='false';
    this.config.$maxFileSize='500000';
    this.config.$url='/test/fileupload';

    this.file = new OlibFileupload;
    this.file.$idx=1;
    this.file.$filePath='assets/img/sample.jpg';
    this.file.$fileSize=20000;
    this.file.$realFileName='sample.jpg';
    this.file.$viewFileName='testfile';
  }

  onBeforeSend(event){
    if(this.config.$credentials && this.config.$authToken){
      event.xhr.setRequestHeader("Authorization", `Bearer ${this.config.$authToken}`);
    }
  }

  onUpload(event) {
    alert("file uploaded!");
    this.olibfile.upload();
  }

  deleteFile(file : OlibFileupload){
    if(confirm('delete file? '+file.$viewFileName)){
      this.file = null;
    }
  }
}
```

# Html
```html
<div class="custom_file">
    <p-fileUpload 
      #olibfile 
      [withCredentials]="config.$credentials" 
      name="file" 
      [url]="config.$url"
      (onUpload)="onUpload($event)" 
      (onBeforeSend)="onBeforeSend($event)" 
      [accept]="config.$accept" 
      [maxFileSize]="config.$maxFileSize"
      styleClass="filebox" 
      [showUploadButton]="false"
      [showCancelButton]="false">

      <ng-template pTemplate="content">
        <div *ngIf="file" class="img_edit">
          <img *ngIf="file" [src]="file.$filePath" style="width: 140px;">
        </div>

        <div *ngIf="file" class="upload_edit fs12">
          {{file.$viewFileName}}<br /> {{file.$fileSize}}
          <button type="button" class="ui-button ui-button-icon-only btn-danger" (click)="deleteFile(file)"></button>
        </div>
      </ng-template>
    </p-fileUpload>
  </div>
```