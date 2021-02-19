---

layout: about
title: Install Codeigniter4
parent: Codeigniter4
grand_parent: Framework
nav_order: 1
has_children: false
has_toc: false

---

# Install
## Reqirements
1. PHP 7.3 or later
2. PHP extensions installed: intl and mbstring extension are installed
3. PHP extension enabled: `php-json`, `php-mysqlnd, and `php-xml`
4. `libcurl` installed for CURL requests
A database is required for most web application programming. Currently supported databases are:
* MySQL (5.1+) via the MySQLi driver
* PostgreSQL via the Postgre driver
* SQLite3 via the SQLite3 driver
* MSSQL via the SQLSRV driver (version 2005 and above only)

Not all of the drivers have been converted/rewritten for CodeIgniter4. The list below shows the outstanding ones.
* MySQL (5.1+) via the pdo driver
* Oracle via the oci8 and pdo drivers
* PostgreSQL via the pdo driver
* MSSQL via the pdo driver
* SQLite via the sqlite (version 2) and pdo drivers
* CUBRID via the cubrid and pdo drivers
* Interbase/Firebird via the ibase and pdo drivers
* ODBC via the odbc and pdo drivers (you should know that ODBC is actually an abstraction layer)


## Install with composer

### Setup Installation
For a new Codeigniter4 installation, you can use the App starter that holds a skeleton application, with a composer dependency on the latest released version of the framework.

In the folder you wish to work on, run this command where `webapp` on this example will be your root project:
```bash
composer create-project codeigniter4/appstarter webapp
```

If you dont want the phpunit or just wanting to install the framework, add `--no-dev` at the end:
```bash
composer create-project codeigniter4/appstarter webapp --no-dev
```

