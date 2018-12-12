# Laravel H5P Package 
A copy of the HP5 Laravel package that does not exist on Bitbucket anymore.
Fixed the HP5 dependencies to stop it breaking. I am looking for some help with this, the package works as is but ideally you should be able to update the h5p dependencies, currently this is not possible.

A [Wiki](https://github.com/garethredfern/laravel-h5p/wiki) has been created to put some initial notes together.

## Installation

```bash
composer require garethredfern/laravel-h5p
```

```bash
php artisan vendor:publish
```

```bash
php artisan migrate
```

```php
'classmap': [
    "vendor/h5p/h5p-core/h5p-default-storage.class.php",
    "vendor/h5p/h5p-core/h5p-development.class.php",
    "vendor/h5p/h5p-core/h5p-event-base.class.php",
    "vendor/h5p/h5p-core/h5p-file-storage.interface.php",
    "vendor/h5p/h5p-core/h5p.classes.php",
    "vendor/h5p/h5p-editor/h5peditor-ajax.class.php",
    "vendor/h5p/h5p-editor/h5peditor-ajax.interface.php",
    "vendor/h5p/h5p-editor/h5peditor-file.class.php",
    "vendor/h5p/h5p-editor/h5peditor-storage.interface.php",
    "vendor/h5p/h5p-editor/h5peditor.class.php"
],
```

```php
'providers' => [
    Chali5124\LaravelH5p\LaravelH5pServiceProvider::class,
];
```


Create a vendor directory if it doesn't exist in your public/assets folder, then symlink to the `h5p` directory in your storage folder. You can set your public path in the config/laravel-h5p file.

```bash
cd public/assets/vendor
ln -s ../../../storage/h5p
```
