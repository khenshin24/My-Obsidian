
"FILTER"
user = [
	{id :'1' , name : 'John',isActive : true},
	{id :'2' , name : 'ken',isActive : true},
	{id :'3' , name : 'kenny',isActive : true},
];
users$ = of(this.users)
usernames$ = this.users.pipe(map((users => users.map(users) => user.name)));
filteredUsers$ = this.users$.pipe(filter((users) => user.isActive))); 
//will create a array of names

of mean can convert to plane data



div *ngFor = "let user of filteredUsers$ | async">
 {{username.name}}
div

result with true isActive
john 
ken
kenny
