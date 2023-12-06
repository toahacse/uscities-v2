### Installation

Clone the repository
```sh
git clone https://github.com/toahacse/uscitiesServer.git
```

Switch to the repo folder
```sh
cd uscitiesServer
```

Install all the dependencies using composer
```sh
composer install
```

Copy the example env file and make the required configuration changes in the .env file

```sh
cp .env.example .env
```
Generate a new application key

```sh
php artisan key:generate
```
publish vendor 
```sh
php artisan vendor:publish --provider="Toaha\Admin\AdminLTE\Providers\AdminLTEServiceProvider" --force
```
```sh
php artisan vendor:publish --provider="Toaha\UsCitiesAdmin\Providers\UsCitiesAdminServiceProvider" --force
```

Run the database migrations (**Set the database connection in .env before migrating**)

```sh
php artisan migrate 
```
Run the cache clear
```sh
php artisan optimize 
```
Start the local development server
```sh
php artisan serve 
```
You can now access the server at http://localhost:8000
