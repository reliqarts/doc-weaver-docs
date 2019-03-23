# Installation

Install via composer; in console: 
```bash
composer require reliqarts/laravel-docweaver
``` 
or require in *composer.json*:
```json
{
    "require": {
        "reliqarts/laravel-docweaver": "^2.0"
    }
}
```
then run `composer update` in your terminal to pull it in.

Ensure that your applications public storage directory is linked and accessible via the browser.

```bash 
php artisan storage:link
```
see: https://laravel.com/docs/master/filesystem

Finally, publish package resources and configuration:

```bash
php artisan vendor:publish --provider="ReliqArts\Docweaver\ServiceProvider"
``` 

You may opt to publish only configuration by using the `docweaver-config` tag:

```bash
php artisan vendor:publish --provider="ReliqArts\Docweaver\ServiceProvider" --tag="docweaver-config"
``` 