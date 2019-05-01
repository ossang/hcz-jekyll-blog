# Component
---
```typescript
export class TableSampleComponent extends OlibTableAbstract {

  constructor(
    private service : TableSampleService
  ) { 
    super();
  }
  
  // 칼럼 초기 설정 
  initializeCols() {
    this.cols = new Array;
    this.cols.push(new OlibTableColsModel("id","No","5%",false,false,false));
    this.cols.push(new OlibTableColsModel("name","Name","25%",true,true,false));
    this.cols.push(new OlibTableColsModel("phone","Phone","25%",true,false,false));
    this.cols.push(new OlibTableColsModel("email","Id","45%",true,false,false));
  }
  
  // 테이블 데이터 설정
  initializeDatas() {
    this.datas = new Array;
    this.service.getSampleData().subscribe(res=>{
      this.setTableDatas(res.data);
    })
  }
  
  // 테이블 옵션 설정
  initializeOptions() {
    this.options = new OlibTableOptionModel();
    this.options.$isCheckbox=false;
    this.options.$isFilter=false;
    this.options.$isSort=true;
    this.options.$isPaginator=true;
    this.options.$isExport=false;
    this.options.$rowsPerPage=[10,20,30];
    this.options.$isCustom=false;
  }
}
```
# Html
---
```html
<olib-table [cols]="cols" [datas]="datas" [options]="options"></olib-table>
```