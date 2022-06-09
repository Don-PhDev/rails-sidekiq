# Rails 7 with Sidekiq

Sidekiq allows Rails to launch any task in the background.
Let's see how, from zero to production.

## Prerequisites

Here are the tools we will use in this tutorial :

* Ruby version

```bash
  ruby -v
  ruby 3.1.1p18 // at least version 3
```
* npm version

```bash
  npm -v
  8.12.1 // at least version 7.1
```

* Yarn version

```bash
  yarn -v
  1.22.15 // at least 1.22.10
```

* PostgreSQL version

```bash
  psql --version
  psql (PostgreSQL) 14.2
```

* Redis

  Run to determine if redis is running

```bash
  redis-cli ping
```

* Foreman

```bash
  foreman -v
  0.87.2
```
