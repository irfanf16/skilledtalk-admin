# SkilledTalk Admin Panel

> **Laravel** back-office panel for managing the [SkilledTalk](https://github.com/irfanf16/skilledtalk) professional marketplace. Administrators manage users, consultations, withdrawals, job listings, and platform analytics through a unified dashboard.

![Laravel](https://img.shields.io/badge/Laravel-8-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

---

## Overview

This panel shares the same database as the main `skilledtalk` application. Admins have full read/write access to all platform data without the user-facing restrictions applied to regular accounts.

```
skilledtalk        — Customer-facing web app + mobile API
skilledtalk-admin  — THIS REPO — Admin back-office
(shared MySQL DB)
```

---

## Features

### User & Professional Management
- View, edit, activate, suspend, or permanently ban user accounts
- Verify professional credentials and skill endorsements
- Review profile reports and content moderation flags

### Job Listing Management
- Moderate job listings posted by users
- Remove inappropriate or spam job posts
- View applicant counts per listing

### Consultation & Booking Management
- View all scheduled and past consultations
- Resolve disputes between consultants and clients
- View Twilio session records

### Payment & Withdrawal Management
- Approve or decline professional withdrawal requests
- View Stripe subscription and payment records
- Monitor wallet balances per user
- Export financial reports

### Platform Analytics
- User growth and engagement metrics
- Consultation volume and revenue trends
- Subscription conversion rates
- Active user, post, and group counts

### Review & Rating Management
- Moderate professional reviews
- Remove fake or policy-violating reviews

---

## Database

Uses the shared `skilledtalk` database. Key tables:

| Table | Admin Access |
|---|---|
| `users` / `profiles` | Full CRUD, status management |
| `consultations` | Read + dispute resolution |
| `withdrawals` | Update `is_approved` status |
| `user_subscriptions` | Read + manual override |
| `post_jobs` / `job_applicants` | Read + delete |
| `posts` / `reflections` | Read + moderation delete |
| `groups` / `pages` | Read + suspend |

---

## Getting Started

```bash
composer install
cp .env.example .env
# Point DB_ to the same database as the main skilledtalk app
php artisan key:generate
php artisan serve
```

## Related Repositories

| Repo | Purpose |
|---|---|
| `skilledtalk` | Main platform (shared database) |
