# library-management

Library Management System - Ruby on Rails

## Features

- Signup/Login users
- Books CRUD
- Mail book details to user (Async)
- Subject-wise Categorization of Books

## Installation

        bundle install

        rake db:create

        rake db:migrate

        rails s

## Usage

- Update the database.yml for postgres

- Setup library-management database

```ruby
    $ rake db:create
    $ rake db:migrate
```

1. Generate Book and Subject model

```ruby
    $ rails generate model Book
    $ rails generate model Subject
```

2. Generate Book and Subject migration

```ruby
    $ rails generate migration books
    $ rails generate migration subjects

    $ rails db:migrate
```

3. Generate controller

```ruby
    $ rails generate controller Book
```

4. Add Carrierwave for image storage

```ruby
    $ rails generate uploader Image

    $ rails generate migration add_image_to_books image:string

    $ rake db:migrate
```

5. Adding Devise and User

https://guides.railsgirls.com/devise

```ruby
    $ bundle install
    $ rails g devise:install
```

Ensure you have defined default url options in your environments files. Open up config/environments/development.rb and add this line:

```ruby
   config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
```

```ruby
    $ rails g devise user
    $ rails db:migrate
```

6. Add ActionMailer

```ruby
    $ rails generate mailer UserMailer
```
