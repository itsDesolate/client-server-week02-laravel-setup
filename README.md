# Client-Server Technologies – Laravel Environment Setup

## 1. Project Title

**Client-Server Technologies – Laravel Environment Setup**

**Student Name:** Jaime Victorio M. Flores
**Student Number:** 0118-4107
**Course:** ITST 302 – Client-Server Technologies
**Section:** BSIT - 3A WAM
**Subject:** Client-Server Technologies
**Current Date:** August 8, 2026

---

## 2. Introduction

Laravel is a modern PHP web application framework used to develop organized, secure, and maintainable web applications. It provides features such as routing, database interaction, migrations, sessions, validation, and application configuration.

Client-Server Technologies is important because it explains how clients and servers communicate when delivering web applications. A web browser sends requests to a server, and the server processes those requests and returns responses. Laravel provides a structured environment for developing applications based on this client-server model.

The purpose of this project is to configure a Laravel development environment, verify the required software, create a Laravel application, connect it to a MySQL database, customize its homepage, and use Git and GitHub for version control and project management.

---

## 3. Objectives

The objectives achieved during this activity are:

1. Install and verify PHP for Laravel development.
2. Install and verify Composer as the PHP dependency manager.
3. Install and verify the Laravel installer.
4. Install and verify Git for version control.
5. Install and verify MySQL as the database management system.
6. Install Visual Studio Code as the development environment.
7. Create and run a Laravel application.
8. Configure Laravel to use a MySQL database.
9. Customize the Laravel homepage with student information.
10. Use Git and GitHub to manage and publish the project.

---

## 4. Development Environment

| Component          | Version / Information  |
| ------------------ | ---------------------- |
| Operating System   | Microsoft Windows 10   |
| PHP                | 8.5.9                  |
| Laravel            | 13.24.0                |
| Composer           | 2.10.2                 |
| Git                | Installed and verified |
| MySQL              | 8.0.46                 |
| Visual Studio Code | See VS Code screenshot |
| Frontend Stack     | Blade                  |
| Database           | MySQL                  |
| Local Server       | PHP Artisan Serve      |

---

## 5. Installation Steps

### Step 1 – Install PHP

PHP was installed and configured on the Windows computer.

The installation was verified using:

```powershell
php -v
```

The PHP version was successfully displayed in the terminal.

### Step 2 – Install Composer

Composer was installed as the dependency manager for PHP projects.

The installation was verified using:

```powershell
composer -V
```

### Step 3 – Install Laravel

The Laravel installer was installed and verified using:

```powershell
laravel -V
```

Laravel was successfully detected by the terminal.

### Step 4 – Install Git

Git was installed for source control and project version management.

The installation was verified using:

```powershell
git --version
```

### Step 5 – Install MySQL

MySQL was installed as the database management system.

The installation was verified using:

```powershell
mysql --version
```

### Step 6 – Install Visual Studio Code

Visual Studio Code was installed and used to open the Laravel project.

The Laravel project was opened in Visual Studio Code from:

```text
C:\Users\JF\Desktop\hello-laravel
```

### Step 7 – Create the Laravel Project

The Laravel project was created using:

```powershell
laravel new hello-laravel
```

During project creation, no starter kit was selected and Blade was selected as the frontend stack.

### Step 8 – Install Composer Dependencies

The initial Laravel installation encountered a missing PHP `fileinfo` extension. After correcting the PHP configuration, Composer dependencies were installed using:

```powershell
composer install
```

The Laravel dependencies were successfully installed.

### Step 9 – Configure the Database

The Laravel `.env` file was configured to use MySQL.

The database configuration included:

```text
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=hello_laravel
```

The PHP MySQL PDO extension was verified using:

```powershell
php -m | findstr /I "pdo_mysql"
```

The terminal displayed:

```text
pdo_mysql
```

### Step 10 – Run Database Migrations

Laravel migrations were executed using:

```powershell
php artisan migrate
```

The migrations completed successfully and created the required Laravel database tables.

### Step 11 – Run Laravel

The Laravel development server was started using:

```powershell
php artisan serve
```

The application was opened at:

```text
http://127.0.0.1:8000
```

### Step 12 – Customize the Homepage

The default `welcome.blade.php` view was customized to display:

* Student Name
* Student Number
* Course
* Section
* Subject
* Current Date

The customized homepage successfully displayed the required student information.

### Step 13 – Configure Git

Git was initialized in the Laravel project.

The project files were added to Git and committed. The main branch was configured as `main`.

### Step 14 – Push the Project to GitHub

The local project was connected to the GitHub repository:

**client-server-week02-laravel-setup**

The Laravel project, README, screenshots, and license were prepared for the public GitHub repository.

---

## 6. Project Structure

### `app/`

Contains the main application code, including models, controllers, and service providers.

### `routes/`

Contains route definitions for the Laravel application. The `web.php` file contains the web routes.

### `resources/`

Contains frontend resources such as Blade views, CSS, and JavaScript files.

### `public/`

Contains publicly accessible files and the main Laravel entry point, `index.php`.

### `config/`

Contains configuration files for the Laravel application, including database, session, cache, filesystem, and application settings.

### `database/`

Contains migrations, factories, and seeders used for database operations.

### `bootstrap/`

Contains files used to initialize and bootstrap the Laravel application.

### `storage/`

Contains application-generated files such as logs, cached files, and sessions.

### `tests/`

Contains automated tests for the Laravel application.

---

## 7. Problems Encountered

### Problem 1 – Missing PHP `fileinfo` Extension

During the initial Laravel project installation, Composer reported that the PHP `fileinfo` extension was missing.

The error indicated that `league/flysystem-local` required the `fileinfo` PHP extension.

### Problem 2 – Missing MySQL PDO Driver

After configuring Laravel to use MySQL, Laravel initially displayed:

```text
could not find driver
```

This occurred because the PHP MySQL PDO driver was not enabled.

### Problem 3 – Missing SQLite Database

Laravel initially attempted to use SQLite and reported that the SQLite database file did not exist.

The project was subsequently configured to use MySQL.

### Problem 4 – Git Repository Not Initialized

The first attempt to use `git status` resulted in:

```text
fatal: not a git repository
```

The Laravel project had not yet been initialized as a Git repository.

---

## 8. Solutions

### Solution to Problem 1

The PHP configuration was checked and the required `fileinfo` extension was enabled.

The PHP modules were verified using:

```powershell
php -m
```

The output confirmed that `fileinfo` was available.

### Solution to Problem 2

The PHP MySQL PDO extension was enabled.

It was verified using:

```powershell
php -m | findstr /I "pdo_mysql"
```

The terminal displayed:

```text
pdo_mysql
```

After enabling the driver, Laravel was able to connect to MySQL and the migrations completed successfully.

### Solution to Problem 3

The `.env` configuration was changed from SQLite to MySQL.

The MySQL database `hello_laravel` was selected as the application's database.

The database migrations were then successfully executed using:

```powershell
php artisan migrate
```

### Solution to Problem 4

Git was initialized in the Laravel project.

The project files were added and committed. The local repository was then connected to GitHub, the branch was changed to `main`, and the project was pushed to the public repository.

---

## 9. Screenshots

The project contains eight screenshots documenting the installation and development process.

### 1. PHP Version

**File:** `screenshots/php-version.PNG`

Shows the installed PHP version.

### 2. Composer Version

**File:** `screenshots/composer-version.PNG`

Shows the installed Composer version.

### 3. Laravel Version

**File:** `screenshots/laravel-version.PNG`

Shows the installed Laravel version.

### 4. Git Version

**File:** `screenshots/git-version.PNG`

Shows the installed Git version.

### 5. MySQL Version

**File:** `screenshots/mysql-version.PNG`

Shows the installed MySQL version.

### 6. Visual Studio Code

**File:** `screenshots/vscode.PNG`

Shows the Laravel project opened in Visual Studio Code.

### 7. Laravel Artisan Server

**File:** `screenshots/artisan-serve.PNG`

Shows the Laravel development server running at `http://127.0.0.1:8000`.

### 8. Customized Laravel Homepage

**File:** `screenshots/hello-laravel-homepage.PNG`

Shows the customized Laravel homepage containing the required student information.

---

## 10. Reflection

This activity helped me understand the practical requirements for setting up a Laravel development environment and how the different tools used in web development work together. I installed and verified PHP, Composer, Laravel, Git, MySQL, and Visual Studio Code before creating and configuring my Laravel project. This showed me that modern web development depends on several tools and services being correctly installed and configured.

One of the most important things I learned was how PHP extensions affect Laravel and Composer. During the installation, I encountered an error because the `fileinfo` extension was missing. I later encountered another error when Laravel could not find the MySQL PDO driver. These problems taught me that installation errors can be caused by PHP configuration rather than by Laravel itself. Checking the installed PHP modules and enabling the required extensions helped me understand how PHP works with external libraries and databases.

I also learned how Laravel connects to a database through the `.env` configuration file. After changing the database configuration to MySQL and enabling the `pdo_mysql` extension, I successfully ran Laravel migrations. This demonstrated how Laravel can create and manage database structures through migration files.

Another important part of the activity was learning Git and GitHub. I initialized a Git repository, created meaningful commits, changed the branch to `main`, connected the project to GitHub, and pushed the project to a public repository. This experience showed me how version control can be used to track project development and maintain a reliable history of changes.

Laravel is important in client-server development because it provides a structured framework for handling client requests, application logic, database operations, and server responses. Its routing, views, models, migrations, and configuration features make it easier to organize web applications.

The knowledge I gained from this activity will help me in future software development projects because I now understand how to configure a development environment, troubleshoot installation problems, build a Laravel application, connect it to a database, and manage the project using Git and GitHub. These skills provide a strong foundation for developing larger Laravel applications in the future.

---

## 11. References

Laravel. (2026). *Laravel documentation*. https://laravel.com/docs

PHP Documentation Group. (2026). *PHP documentation*. https://www.php.net/docs.php

Composer. (2026). *Composer documentation*. https://getcomposer.org/doc/

Git. (2026). *Git documentation*. https://git-scm.com/doc

Oracle. (2026). *MySQL documentation*. https://dev.mysql.com/doc/

Microsoft. (2026). *Visual Studio Code documentation*. https://code.visualstudio.com/docs

---

## GitHub Submission

**Repository Name:** `client-server-week02-laravel-setup`

**Repository Visibility:** Public

The repository contains:

* Laravel Project
* `README.md`
* `screenshots/`
* `LICENSE`
* `.gitignore`
* Git commit history

---

## Commit History

The project uses meaningful commits to document major development milestones.

1. `feat: initialize Laravel project`
2. `docs: add installation screenshots`
3. `docs: add project license`
4. `docs: add project README`
5. `feat: customize homepage`

---

## LinkedIn Portfolio Activity

A professional LinkedIn post will be created to document the Laravel environment setup, technologies installed, customized application, GitHub repository, and lessons learned from the activity.
