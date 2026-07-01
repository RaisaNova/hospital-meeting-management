
# Contributing Guide

Thank you for considering contributing to the **Hospital Meeting Management System**. We appreciate your time and effort in helping improve this project.

Please read the following guidelines before submitting your contribution.

---

# Prerequisites

Before getting started, make sure you have the following installed on your machine:

* PHP 8.3 or later
* Composer
* MySQL or MariaDB
* Git
* Laravel CLI (optional but recommended)

---

# Getting Started

## 1. Fork the Repository

Fork this repository to your own GitHub account.

## 2. Clone Your Fork

```bash
git clone https://github.com/your-username/hospital-meeting-management.git
cd hospital-meeting-management
```

## 3. Install Dependencies

```bash
composer install
```

## 4. Configure Environment

Copy the example environment file.

```bash
cp .env.example .env
```

For Windows:

```bash
copy .env.example .env
```

Generate the application key.

```bash
php artisan key:generate
```

---

# Configure Database

Update your `.env` file with your database credentials.

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=hospital_meeting_management
DB_USERNAME=root
DB_PASSWORD=
```

Run the database migrations.

```bash
php artisan migrate
```

If seeders are available:

```bash
php artisan db:seed
```

or

```bash
php artisan migrate --seed
```

---

# Running the Application

Start the Laravel development server.

```bash
php artisan serve
```

Visit:

```
http://localhost:8000
```

---

# Creating a Branch

Please do **not** commit directly to the `main` branch.

Create a feature or bug-fix branch instead.

```bash
git checkout -b feature/feature-name
```

Examples:

```bash
git checkout -b feature/meeting-calendar
git checkout -b feature/doctor-availability
git checkout -b fix/login-validation
```

---

# Coding Standards

Please follow Laravel best practices.

### Backend

* Follow PSR-12 coding standards.
* Keep controllers thin.
* Move business logic into Services or Actions when appropriate.
* Use Form Request classes for validation.
* Prefer Eloquent relationships over raw SQL.
* Write meaningful variable and method names.

### Blade Templates

* Keep views clean and readable.
* Reuse layouts and Blade components whenever possible.
* Avoid placing business logic inside Blade files.

---

# Commit Messages

Use clear and descriptive commit messages.

Recommended format:

```text
type: short description
```

Examples:

```text
feat: add doctor availability management
fix: resolve meeting schedule validation
docs: update installation guide
refactor: simplify appointment service
style: improve Blade formatting
```

---

# Push Your Changes

```bash
git push origin feature/feature-name
```

---

# Pull Request Guidelines

Before opening a Pull Request, please ensure that:

* Your code builds successfully.
* All existing functionality still works.
* No unnecessary files are included.
* Your branch is up to date with `main`.
* Your Pull Request contains a clear description of the changes.

---

# Code Review Checklist

Before submitting your contribution, verify that:

* Code follows Laravel conventions.
* There are no syntax errors.
* Validation is implemented where necessary.
* Database migrations work correctly.
* Blade views are responsive and properly formatted.
* Documentation has been updated if applicable.

---

# Things to Avoid

Please do **not**:

* Commit the `.env` file.
* Commit the `vendor/` directory.
* Commit generated cache files.
* Push directly to the `main` branch.
* Remove or modify existing functionality without discussion.

---

# Reporting Issues

When reporting a bug, please include:

* A clear description of the issue.
* Steps to reproduce.
* Expected behavior.
* Actual behavior.
* Screenshots (if applicable).
* PHP and Laravel versions.

---

# Suggesting Features

Feature requests are welcome.

Please include:

* The problem you want to solve.
* Your proposed solution.
* Any additional context or mockups.

---

# Questions

If you have any questions, feel free to open an Issue or start a discussion in the repository.

---

Thank you for contributing to the **Hospital Meeting Management System**. Your contributions help make this project better for everyone.
