## Laravel Excel v2.1.* for Laravel 5 - Fork of Maatwebsite/Laravel-Excel to keep using v2 with php >=7.4


---

```php
Excel::create('Laravel Excel', function($excel) {

    $excel->sheet('Excel sheet', function($sheet) {

        $sheet->setOrientation('landscape');

    });

})->export('xls');
```

---

# Installation

Require this package in your `composer.json` and update composer. This will download the package and PHPExcel of PHPOffice.

```php
composer require "convenia/excel:~2.2.*"
```

In Laravel 5.5 or higher, this package will be automatically discovered and you can safely skip the following two steps.

If using Laravel 5.4 or lower, after updating composer, add the ServiceProvider to the providers array in `config/app.php`

```php
Maatwebsite\Excel\ExcelServiceProvider::class,
```

You can use the facade for shorter code; if using Laravel 5.4 or lower, add this to your aliases:

```php
'Excel' => Maatwebsite\Excel\Facades\Excel::class,
```

The class is bound to the ioC as `excel`

```php
$excel = App::make('excel');
```

To publish the config settings in Laravel 5 use:

```php
php artisan vendor:publish --provider="Maatwebsite\Excel\ExcelServiceProvider"
```

This will add an `excel.php` config file to your config folder.

# Documentation

The complete documentation can be found at: [https://laravel-excel.maatwebsite.nl/docs](https://laravel-excel.maatwebsite.nl/docs)

# License

MIT

