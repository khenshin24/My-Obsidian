navigation

_nav.ts

{
      title: "Users",
      icon: "user-SB.svg",
      roles: ['SystemAdministrator'],
      route: ['/users'],
      children:[]
    },

app-routing.module.ts
     {
        path: 'users',
        loadChildren: () => import('./users/users.module').then((m) => m.UsersModule)
      } 
note try to click the button to change the url

ng g c users/views/user-list

const routes: Routes = [
  {
    path: '',
    component : UserListComponent ,
    children:[
      // {
      //   path:'',
      //   component: UserComponent,
      //   data: {
      //     title: 'Add User'
      //   },
      // },
    ]
  }
];


output 

child to parent --- use event emitter

Input
parent to child --



dependent Dropdown
	once you click the parent selection the child selection will find the dependant id to the parents 



create folder with module and routing
		ng g m users --routing













