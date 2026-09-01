books
	prop title,author
reviews
	 prop review,rating


relatation ship 2 tablse

```php
	$table->foreignId('book_id)->constrained()->cascadeOnDelete();
```


```php

public function good(){
	return $this->state(function (array $attribute){
			return [
				'rating' => fake()->numberBetween(4-5)
			]
	})
}
average(2,5)
bad(1,3)
```