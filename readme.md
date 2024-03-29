<img src="https://github.com/kkamara/useful/blob/main/php-reactjs-boilerplate.png?raw=true" alt="php-reactjs-boilerplate.png" width=""/>

<img src="https://github.com/kkamara/useful/blob/main/php-reactjs-boilerplate2.png?raw=true" alt="php-reactjs-boilerplate2.png" width=""/>

# Laravel API Resources [![API](https://github.com/kkamara/laravel-api-resources/actions/workflows/build.yml/badge.svg)](https://github.com/kkamara/laravel-api-resources/actions/workflows/build.yml)

(14-Mar-2024) A Laravel 11.x app with Reactjs Redux.

* [Using Thunder Client?](#thunder-client)

* [Installation](#installation)

* [Usage](#usage)

* [Api Documentation](#api-documentation)

* [Unit Tests](#unit-tests)

* [Browser Tests](#browser-tests)

* [Misc](#misc)

* [Contributing](#contributing)

* [License](#license)

<a name="thunder-client"></a>
## Using Thunder Client?

[Thunder client](https://www.thunderclient.com/) Visual Studio Code extension.

[thunder-collection_Laravel API Resources.json](https://github.com/kkamara/laravel-api-resources/blob/main/database/thunder-collection_Laravel%20API%20Resources.json)

## Installation

* [https://laravel.com/docs/11.x/installation](https://laravel.com/docs/11.x/installation)
* [https://laravel.com/docs/11.x/vite#main-content](https://laravel.com/docs/11.x/vite#main-content)

```bash
# Create our environment file.
cp .env.example .env
# Install our app dependencies.
composer i
# Using Docker?
# Refer to Laravel Sail documentation: 
# https://laravel.com/docs/11.x/sail#main-content
# Not using Docker?
php artisan key:generate
# Before running the next command:
# Update your database details in .env
php artisan migrate --seed
npm install
npm run build
```

## Usage

```bash
php artisan serve --port=3000
```

#### Using UserCollection results in duplication of "success" key in data array

```json
{
    "data": [
        {
            "success": true,
            "data": {
                "first_name": "Jason",
                "last_name": "Herzog",
                "email": "saufderhar@example.org",
                "created_at": "2024-03-14T21:47:17.000000Z",
                "updated_at": "2024-03-14T21:47:17.000000Z"
            }
        },
        {
            "success": true,
            "data": {
                "first_name": "Amira",
                "last_name": "Wiza",
                "email": "jledner@example.net",
                "created_at": "2024-03-14T21:47:17.000000Z",
                "updated_at": "2024-03-14T21:47:17.000000Z"
            }
        }
    ]
}
```

[See fix in Laravel API Resources 2](https://github.com/kkamara/laravel-api-resources-2?tab=readme-ov-file#we-get-the-following-successful-response-for-getallusers-request).

## Api Documentation

```bash
php artisan route:list
# output
...
POST       api/user ............................ login › Api\UserController@login
GET|HEAD   api/user/authorize .................. Api\UserController@authorizeUser
POST       api/user/register ................... Api\UserController@register
...
```

View the api collection [here](https://documenter.getpostman.com/view/17125932/TzzAKvVe).

## Unit Tests

```bash
php artisan test --filter=Api
```

View the unit test code [here](https://raw.githubusercontent.com/kkamara/php-reactjs-boilerplate/main/tests/Unit/Api/UsersTest.php).

## Browser Tests

```bash
alias sail='vendor/bin/sail'
sail dusk
```

## Misc

[See MRVL Desktop.](https://github.com/kkamara/mrvl-desktop)

[See MRVL Web.](https://github.com/kkamara/mrvl-web)

[See Github to Bitbucket Backup Repo Updater.](https://github.com/kkamara/ghbbupdater)

[See PHP Docker Skeleton.](https://github.com/kkamara/php-docker-skeleton)

[See Laravel 10 API 3.](https://github.com/kkamara/laravel-10-api-3)

[See movies app.](https://github.com/kkamara/movies)

[See food nutrition facts search web app.](https://github.com/kkamara/food-nutrition-facts-search-web-app)

[See ecommerce web.](https://github.com/kkamara/ecommerce-web)

[See city maps mobile.](https://github.com/kkamara/city-maps-mobile)

[See ecommerce mobile.](https://github.com/kkamara/ecommerce-mobile)

[See crm.](https://github.com/kkamara/crm)

[See birthday currency.](https://github.com/kkamara/birthday-currency)

[See PHP scraper.](https://github.com/kkamara/php-scraper)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[BSD](https://opensource.org/licenses/BSD-3-Clause)
