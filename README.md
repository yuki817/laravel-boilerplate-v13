# Laravel Boilerplate

A modern Laravel 13 boilerplate with React, Inertia.js, and a full local development environment.

## Stack

**Backend**

- PHP 8.5, Laravel 13
- Laravel Fortify (authentication)
- Laravel Wayfinder (typed route functions)
- Pest 4 (testing)
- Pint (code style)

**Frontend**

- React 19, TypeScript 6
- Inertia.js v3
- Tailwind CSS v4
- Vite 8
- ESLint 9, Prettier 3

**Local Development**

- Laravel Sail (Docker)
- MariaDB 11
- Mailpit (email preview at http://localhost:8025)
- phpMyAdmin (at http://localhost:8080)
- Laravel Telescope (at http://localhost/telescope)
- Laravel Debugbar

## Getting Started

**1. Install dependencies**

```bash
composer install
npm install
```

**2. Configure environment**

```bash
cp .env.example .env
php artisan key:generate
```

**3. Start Sail**

```bash
./vendor/bin/sail up -d
```

**4. Run migrations**

```bash
sail artisan migrate
```

**5. Start the dev server**

```bash
sail npm run dev
```

## Development

```bash
# Run tests
sail artisan test

# Lint PHP
composer run lint

# Lint JS/TS
npm run lint

# Format
npm run format

# Type check
npm run types:check
```

Pre-commit hooks run automatically via Husky — ESLint, Prettier, and Pint will fix staged files on every commit.

## CI

GitHub Actions runs the test suite on every push and pull request to `main`.
