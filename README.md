# errors-and-solutions-laravel


#### Live Server issue on Filament login route post method doesn't support, or 
#### The POST method is not supported for route admin/login. Supported methods: GET, HEAD.

![image](https://github.com/mabdusshakur/errors-and-solutions-laravel/assets/82134930/31710ff2-c6a9-4320-9e7c-c2409a10df7a)

* Solve 1: php artisan vendor:publish --force --tag=livewire:assets



#### $table->renameColumn('old_name','new_name'); is not working.

* Solve 1: maybe you don't have the package installed : [ composer require doctrine/dbal && composer install ]

#### 419 Page Expired Laravel, or
#### 419 error during postman testing,



* Solve 1: disable the csrf,
* * Laravel 11 : $middleware->validateCsrfTokens(except: ['/*']);
  * ![image](https://github.com/user-attachments/assets/3e514d3b-7683-4aa2-bba2-412697c64969)

#### Base table not found, 500 internal error,

* Solve 1: database table not available, migrate the database.

#### Session table missing on Laravel 11,

* Solve 1 : php artisan make:session-table

#### Unable to connect with STARTTLS: stream_socket_enable_crypto(): SSL operation failed with code 1. OpenSSL Error messages:\nerror:0A000086:SSL routines::certificate verify failed"

* Solve 1 (Temporary ) : in config>mail.php
- 'auth_mode'  => null,
- 'verify_peer' => false,
