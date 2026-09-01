
	use map if the return in back end is 

```json
{
"data" : {
		"id" : 1,
		"name" : "kenny"
	}
}
```
	
	
 you need to transform it to 


```json
{
	"id" : 1,
	"name" : "kenny"
}
```

so you need to use map in rxjs

pip then map no need to subcribe

this.service.getbyId(id)
	.pipe(
	  .map((res:any) => res.data)
	)



- `@Input()` → **Parent → Child**
- `@Output()` → **Child → Parent**
  
  so its not about the button its data flow


check if the data is delayed
Angular lifecycle:

1. Component created
2. `ngOnInit()` runs ❗
3. THEN `@Input()` gets value ❗

first clicked studentId is undefined
then second he gets the data 

use 

ngOnChanges(changes: SimpleChanges): void {
  if (changes['selectedStudentId'] && this.selectedStudentId) {
    this.loadStudentById();
  }
}
