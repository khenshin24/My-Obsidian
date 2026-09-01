``observale 

title = 'angular-observables';

data : any[] = []

//1. Create an observable

//observable

myObservable = new Observable((observable) => {
	observer.next([1,2,3,4,])
});

getAsyncData(){
	//Observer
	//next ,error, complete this is call back function
	this.myObservable.subcribe((val) => {
	this.data = val;
});
	
}

html

<div class="data-list" *ngfor="let x of data">
	{{x}}
</div>

<button (click)="getAsyncData()">Get Data</button>


//observale 

title = 'angular-observables';

data : any[] = []

//1. Create an observable

//observable

myObservable = new Observable((observable) => {
	//observer.next([1,2,3,4,])
	setTimeout(() => {observer.next(1)},1000);
	setTimeout(() => {observer.next(2)},2000);	
	setTimeout(() => {observer.next(3)},3000);
	setTimeout(() => {observer.next(4)},4000);
	setTimeout(() => {observer.next(5)},5000);
});

getAsyncData(){
	//Observer
	//next ,error, complete this is call back function
	this.myObservable.subcribe((val) => {
	this.data.push(val)
});
	
}

html

<div class="data-list" *ngfor="let x of data">
	{{x}}
</div>

<button (click)="getAsyncData()">Get Data</button>