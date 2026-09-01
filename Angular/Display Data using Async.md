Async
user = [
	{id :'1' , name : 'John',isActive : true},
	{id :'2' , name : 'ken',isActive : true},
	{id :'3' , name : 'kenny',isActive : true},
];
users$ = of(this.users)
of mean can convert to plane data

div *ngFor = "let user of users$ | async">
 {{user.name}}
div~
