```"COMBINELATEST"
user = [
	{id :'1' , name : 'John',isActive : true},
	{id :'2' , name : 'ken',isActive : true},
	{id :'3' , name : 'kenny',isActive : true},
];
user$ = new BehaviorSubject<{id:string;name : string} | null>(null)

users$ = of(this.users)
usernames$ = this.users.pipe(map((users => users.map(users) => user.name)));
filteredUsers$ = this.users$.pipe(filter((users) => user.isActive))); 
//will create a array of names
//of mean can convert to plane data


data$ = combineLatest([
	this.users,
	this.usernames,
	this.filteredUsers,
]).pipe(([users.usernames,filteredUsers]))
);


div *ngif = "data | async as data"

	div *ngFor = "let user of data.users | async">
		 {{user.name}}
	div

div *ngFor = "let user of data.userrnames | async">
		 {{username}}
	div

div *ngFor = "let user of data.filteredUsers | async">
		 {{user.name}}
	div
div 