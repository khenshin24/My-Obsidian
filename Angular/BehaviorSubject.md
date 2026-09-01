
```"BehaviorSubject"
user = [
	{id :'1' , name : 'John',isActive : true},
	{id :'2' , name : 'ken',isActive : true},
	{id :'3' , name : 'kenny',isActive : true},
];
user$ = new BehaviorSubject<{id:string;name : string} | null>(null)

//users$ = of(this.users)
//usernames$ = this.users.pipe(map((users => users.map(users) => user.name)));
//filteredUsers$ = this.users$.pipe(filter((users) => user.isActive))); 
//will create a array of names
//of mean can convert to plane data


ngOnInit():void {
	setTimeout(() => {
	this.user$.next({id : '1',name : 'John'});
},2000);
	this.users$.subcribe((suser) => {
	console.log('user',user)
})
}


div *ngif="user$" | async as user"> {{user.name}}div

result if you refresh the web the result it null but after 2 sec the result will 1 and john 
user {id : '1',name : 'John'}