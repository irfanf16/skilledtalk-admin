# SkilledTalk Admin Panel

Admin control panel for the **SkilledTalk** professional skills marketplace. Manages users, job listings, consultations, payments, and platform analytics.

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat&logo=laravel)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=bootstrap)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql)

## Features

- User and professional account management
- Job listing moderation and oversight
- Consultation and booking management
- Payment and withdrawal management
- Platform analytics and reporting
- Review and rating management

> This admin panel shares the same database as the main `skilledtalk` application and provides admin-only routes with middleware protection.

## Getting Started

```bash
composer install
cp .env.example .env && php artisan key:generate
# Point DB_DATABASE to the same database as the main skilledtalk app
php artisan serve
```

## License
MIT
