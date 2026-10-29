# Apoteck 2.0

Apoteck 2.0 is an academic web project for a fictional pharmacy. It was created in 2018 as part of the Integrative Project for the Technical Program in Informatics at IFSC, Lages campus, by Ana Athayde and Jaqueline Oliveira Santos.

The project contains a Portuguese-language storefront prototype with a home page, product category pages for beauty and protection, cosmetics, and hygiene, plus cart, customer registration, and login pages. PHP model and controller files provide an initial structure for customer and login operations. This is a student project, not a production-ready e-commerce system; some pages and server-side flows are incomplete or depend on the original development environment.

## Repository Structure

- `controller/`: PHP controllers for customer and login operations.
- `model/`: Customer and login models, business logic, data access objects, and database connection code.
- `view/html/`: Storefront pages and customer/login forms and handlers.
- `view/css/`: Bootstrap and project stylesheets.
- `view/js/`: Bootstrap, jQuery, Popper, and project scripts.
- `view/img/`: Images used by the storefront, organized into category folders.

## Requirements

- PHP with a web server, such as Apache with PHP enabled.
- MySQL, if you are testing the database-backed parts.

The storefront entry point is `view/html/index.php`. Serve the repository through a PHP-enabled web server and open `/view/html/index.php` in a browser. Opening the PHP file directly from the filesystem will not execute it as a website.

## Database and Configuration

The database connection settings are currently hard-coded in `model/DBConnection.class.php` (`localhost`, database `aluno20`, user `aluno20`, password `aluno`, and port `3306`). Update these values for your local MySQL setup before using code that connects to the database. The repository does not include a database schema or seed data, so the required tables must be created separately.

Some PHP files also contain absolute paths tied to the original hosting setup. In addition, the legacy login handler in `view/html/login/suporte_login.php` uses the removed `mysql_*` PHP extension and must be updated before it can run on modern PHP versions. Customer registration and login should therefore be treated as unfinished and may require environment-specific changes.

## Project Components

- Customer-related classes: `Cliente.class.php`, `ClienteBusiness.php`, `ClienteDAO.class.php`, and `ClienteController.class.php`.
- Login-related classes: `login.class.php`, `loginBusuness.php`, `loginDAO.class.php`, and `loginController.class.php`.
- Shared database connection: `DBConnection.class.php`.
- Front-end assets: Bootstrap, jQuery, Popper, project CSS, JavaScript, and product images under `view/`.

## Contributing

Contributions such as bug fixes, documentation improvements, and modernization of the PHP/database flows are welcome. Before submitting a change, verify it against the PHP and MySQL versions you intend to support and document any required database setup.

