
composer require tymon/jwt-auth

```php
rc/app/  
│  
├── core/ # singleton services (auth, interceptors)  
│ ├── services/  
│ │ └── auth.service.ts  
│ └── interceptors/  
│ └── auth.interceptor.ts  
│  
├── shared/ # reusable components  
│ └── components/  
│ └── sidebar/  
│ ├── sidebar.component.ts  
│  
├── features/  
│ ├── auth/ # AUTH MODULE  
│ │ ├── pages/  
│ │ │ ├── login/  
│ │ │ └── register/  
│ │ ├── auth-routing.module.ts  
│ │ └── auth.module.ts  
│ │  
│ ├── dashboard/ # PROTECTED AREA  
│ │ ├── layout/ # sidebar layout  
│ │ │ ├── dashboard-layout.component.ts  
│ │ │ └── dashboard-layout.html  
│ │ │  
│ │ ├── pages/ # sidebar targets  
│ │ │ ├── home/  
│ │ │ ├── users/  
│ │ │ └── settings/  
│ │ │  
│ │ ├── dashboard-routing.module.ts  
│ │ └── dashboard.module.ts  
│  
└── app-routing.module.ts
```



Cors issue
	in angular 
	 file -> proxy.conf.json
	 change it to api
	 then in service remove the path of localhost/127.0.0 something retain only API
	 add option in angular.json
	 "serve": {
          "builder": "@angular/build:dev-server",
          "options" : {
            "proxyConfig" : "proxy.conf.json"
          },
