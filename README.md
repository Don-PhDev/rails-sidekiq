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

## Create a new Rails 7 app

```bash
  mkdir sidekiqrails && cd sidekiqrails  
  echo "source 'https://rubygems.org'" > Gemfile  
  echo "gem 'rails', '7.0.1'" >> Gemfile  
  bundle install  
  bundle exec rails new . --force -d=postgresql --minimal
```

* Create a default controller
```bash
  echo "class WelcomeController < ApplicationController" > app/controllers/welcome_controller.rb
  echo "end" >> app/controllers/welcome_controller.rb
```

* Create a default route
```bash
  echo "Rails.application.routes.draw do" > config/routes.rb
  echo '  get "welcome/index"' >> config/routes.rb
  echo '  root to: "welcome#index"' >> config/routes.rb
  echo 'end' >> config/routes.rb
```

* Create a default view
```bash
  mkdir app/views/welcome
  echo '<h1>This is h1 title</h1>' > app/views/welcome/index.html.erb
```

## License & Copyright
© 2022 Don Forrest Usbal (Don-PhDev)

Licensed under the [MIT License](LICENSE)
