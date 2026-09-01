
npm install -g @angular/cli


Model
Entity
index.ts -> entity folder
schema -> validation
controller
route
app.ts


error:
		'tsc' is not recognized as an internal or external command,
		operable program or batch file.
	ans: 
		npm install typescript --save-dev


npm run start -> to start the project


model: ParticularModel (singular)
controller: particular.controller.ts (singular)
route: particular.route.ts


columns:

id: 
name: string, max(150), indexed
isPax: boolean, default false
isDays: boolean, default false
isUnitCost: boolean, default false
isQty: boolean, default false

pagawan din ng seeder



logCurrentUser() {

    console.log('=== Current Logged-in User ===');
    console.log('Full Name:', this._authService.user_fullname);
    console.log('Username/Email:', this._authService.username);
    console.log('User ID:', this._authService.userid);
    console.log('Role ID:', this._authService.roleid);
    console.log('Roles:', this._authService.roles);
    console.log('Org Unit:', this._authService.orgUnitName);
    console.log('Org Unit ID:', this._authService.orgUnitId);
    console.log('=================================');
  }



