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
