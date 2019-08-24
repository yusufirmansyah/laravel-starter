# laravel Starter

## Tutorials

#### How to created Laravel Starter from Scratch

## Installation


#### Requirements

https://laravel.com/docs/5.8#server-requirements


#### Install laravel

```
laravel new laravel-starter
```

Enter folder
```
cd laravel-starter
```

Install Depencencies
```
npm install
npm install vue
npm install npm install browser-sync-webpack-plugin@2.0.1
```

Add Browsersync into webpack.mix.js file
```javascript
mix.js('resources/js/app.js', 'public/js')
    .sass('resources/sass/app.scss', 'public/css')
    .browserSync('laravel-starter.test');
```

Compiling Assets (Laravel Mix)
```
npm run dev
```

#### Configuration

Generate .env file
```
cp .env.example .env
```

Edit .env file
```
APP_NAME="Laravel Starter"
APP_URL=http://laravel-starter.test/

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel-starter
DB_USERNAME=username
DB_PASSWORD=password
```

Create Database
```mysql
mysql> create database laravel-starter;
```

Install Laravel Authentication
```php
php artisan make:auth
```

Create tables
```php
php artisan migrate
```

Generate Users Table Seed
```php
php artisan make:seeder UsersTableSeed
```

edit UsersTableSeeder.php file
```php
public function run()
{
    factory(App\User::class, 50)->create();
}
```

edit DatabaseSeeder.php, Add UsersTableSeeder.php seeder
```php
public function run()
{
    $this->call(UsersTableSeeder::class);
}
```

Run artisan db seed
```php
php artisan db:seed
```

