
if you want to change the prop in table 

php artisan make:migration update_table_name

```php
public function up(): void
    {
        Schema::table('teachers', function (Blueprint $table) {
            $table->dropColumn('department'); // old column
            $table->foreignId('departmentId')
                ->constrained('departments')
                ->cascadeOnDelete();
        });
    }

    public function down(): void
    {
        Schema::table('teachers', function (Blueprint $table) {
            $table->dropForeign(['departmentId']);
            $table->dropColumn('departmentId');
            $table->string('department');
        });

    }
```