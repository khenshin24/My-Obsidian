
Crud Naming

| Method    | URI                | Action  | Route Name    |
| --------- | ------------------ | ------- | ------------- |
| GET       | /posts             | index   | posts.index   |
| GET       | /posts/create      | create  | posts.create  |
| POST      | /posts             | store   | posts.store   |
| GET       | /posts/{post}      | show    | posts.show    |
| GET       | /posts/{post}/edit | edit    | posts.edit    |
| PUT/PATCH | /posts/{post}      | update  | posts.update  |
| DELETE    | /posts/{post}      | destroy | posts.destroy |

`
```php 
php artisan make:model Task -m                      : model with migration
php artisan migrate                                 : run migration
php artisan tinker                                  : run query in cmd
php artisan migrate:rollback                        : rollback the last migration
php artisan make:factory nameFactory --model=Model  : factory and seed | use hasFactory in Model factory->databaseSeeder
php artisan db:seed                                 : seed the data
php artisan route:list                              : display all routelist
php artisan migrate:refresh --seed                  : wipe the data then seed
php artisan make:request NameRequest                : reusable form request
php artisan make:controller BookController --ressource 
```
		
##### Function
```php
latest()      : get from the latest data
findOrFail()  : if null return 404 page
create()
update()
delete()
validated()   : validate the entire prop in form 
paginate()
old()         : set in value to retain the data in the input field 
```


```php
//using model binding as a default he will find the primary key which is the id instead of id the parameter use model
Route::get('/tasks/{task}', function (Task $task) {
    return view('show', [
        'task' => $task
    ]);
})->name('tasks.show');
```
#### Links 
Query Builder docs in laravel
https://laravel.com/docs/12.x/queries

Before using the api/ Register the api in Bootstrap/app.php under Web/php


Rule

```php
|Action|Correct Syntax|
|---|---|
|Create new record|`Task::create()`|
|Update existing record|`$task->update()`|
|Delete existing record|`$task->delete()`|
```



live refresh
	add in blade 
	app.layout @vite(['resources/css/app.css', 'resources/js/app.js'])
	 npm run dev
		 other terminal
				php artisan serve

checking for exist data
```php
 public function rules(): array
 {
     return [
         'title' => 'max:255^|required^|unique:tasks,title',
         'description' => 'required'
     ];
 }

 public function messages(): array
 {
     return ['title.unique' => 'Title already Exist'];
 }
```


flash
```php
<div x-data="{flash : true}">
      <div x-show="flash">
         @if (session()->has('success'))
               <div class="relative mb-5 mt-10 rounded border border-green-400 bg-green-100 px-4 py-3 text-lg text-green-700"
                        role="alert">
                     <strong class="font-bold">Success!</strong>
                     <div>{{ session('success') }}</div>
                     <span class="absolute top-0 bottom-0 right-0 py-2 px-2">
                     <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                stroke-width="1.5" @click="flash = false"
                                stroke="currentColor" class="h-6 w-6 cursor-pointer">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                            </svg>
                        </span>
                    </div>
                </div>
                @endif
            </div>
```

error
```php
<div>
   <label for="title">Title</label>
      <input
            type="text"
            name="title"
            value="{{ $task->title ?? old('title') }}"
            @class(['border-red-500' => $errors->has('title')])
            >
            @error('title')
               <p class="error">{{ $message }}</p>
            @enderror
 </div>
```