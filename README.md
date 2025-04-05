```
## Router
```
  _____  _    _ _____             _____             _            
 |  __ \| |  | |  __ \           |  __ \           | |           
 | |__) | |__| | |__) |  ______  | |__) |___  _   _| |_ ___ _ __
 |  ___/|  __  |  ___/  |______| |  _  // _ \| | | | __/ _ \ '__|
 | |    | |  | | |               | | \ \ (_) | |_| | ||  __/ |   
 |_|    |_|  |_|_|               |_|  \_\___/ \__,_|\__\___|_|   
```

**PHP Router**, a simple, powerful, and modern PHP routing class with support for Middlewares and Controllers — now updated for PHP 8.2+ compatibility and actively maintained by [Joy Kalyan](https://joykalyan.guru).

![Tests](https://github.com/joypurchase0/router/actions/workflows/run-tests.yml/badge.svg)

---

### 🔥 Fork Highlights (Joy Kalyan Edition)

- PHP 8.2 deprecation fixes
- Composer package renamed: `joypurchase0/router`
- Drop-in replacement for `izniburak/router` with the same API
- Actively maintained by Joy Kalyan: [joykalyan.guru](https://joykalyan.guru)

---

### ✨ Features
- Supports GET, POST, PUT, DELETE, OPTIONS, PATCH, HEAD, AJAX and ANY request methods
- Easy integration with `symfony/http-foundation`
- Controller support (`HomeController@about`)
- Before and After Middlewares
- Static & Dynamic Routes
- Custom route patterns with RegExp
- Namespace & Route Grouping
- Custom 404 & Exception handling
- Debug mode for dev-friendly errors

---

## 🚀 Install

Install it via Composer:

```
composer require joypurchase0/router
```

Or manually add it to your `composer.json`:

```json
{
  "require": {
    "joypurchase0/router": "^2.0"
  }
}
```

Then run:

```
composer install
```

---

## 🧪 Example Usage

```php
require 'vendor/autoload.php';

use Buki\Router\Router;
use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;

$router = new Router;

// Basic GET route
$router->get('/', function(Request $request, Response $response) {
    return $response->setContent('Hello World');
});

// GET with Controller
$router->get('/test', 'TestController@main');

// Auto-discovered controller routes
$router->controller('/users', 'UserController');

$router->run();
```

---

## 📚 Docs

See original documentation on [Buki\Router Wiki](https://github.com/izniburak/php-router/wiki)  
Changelog available at: [Buki\Router Changelogs](https://github.com/izniburak/php-router/wiki/Changelogs)

---

## 🙌 Credits

- Original Author: [İzni Burak Demirtaş](https://github.com/izniburak) — [Homepage](http://burakdemirtas.org)
- Fork Maintainer: [Joy Kalyan](https://joykalyan.guru) — [GitHub](https://github.com/joypurchase0)

---

## 🤝 Contributing

1. Fork this repo ( https://github.com/joypurchase0/router )
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit changes (`git commit -am 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request 🚀

---

## 📬 Contact

**Joy Kalyan**  
🌐 [joykalyan.guru](https://joykalyan.guru)  
📧 joypurchase0@gmail.com  
🐙 [github.com/joypurchase0](https://github.com/joypurchase0)

---

## 📄 License

[MIT License](http://opensource.org/licenses/MIT)
```
