# Friends App Using Rails

This is a simple Ruby on Rails application that helps manage a list of friends. The app includes authentication using Devise and allows you to store and manage personal information such as first name, last name, email, and phone number.

## Requirements

- Ruby 3.3.7
- Rails 8.0.1

## System Dependencies

Make sure you have the following installed on your system:

- Ruby (version 3.3.7 or higher)
- Rails (version 8.0.1 or higher)
- A supported database (e.g., PostgreSQL, MySQL, SQLite)

## Getting Started

Follow the steps below to get the application up and running on your local machine.

### 1. Install Required Gems

Run the following command to install the required dependencies:

```bash
bundle install
```

### 2. Generate the Home Controller

Create a `home` controller with an `index` action:

```bash
rails g controller home index
```

### 3. Generate the Friend Scaffold

This will create a model, controller, and views for managing friends:

```bash
rails g scaffold Friend first_name:string last_name:string email:string:uniq phone:string:uniq
```

### 4. Add Devise Gem for Authentication

Add `devise` to your Gemfile:

```ruby
gem 'devise'
```

Then install the gem:

```bash
bundle install
```

### 5. Install Devise

Run the following command to install Devise:

```bash
rails g devise:install
```

Follow the instructions shown in the terminal, which include:

- Adding Devise configuration to `config/environments/development.rb`
- Setting the root path to `home#index`
  
```ruby
root "home#index"
```

### 6. Generate Devise Views

To customize the views for Devise, run the following command:

```bash
rails g devise:views
```

### 7. Set Up the Database

Run the following command to create the database and apply migrations:

```bash
rails db:migrate
```

### 8. Generate the User Model

Now, generate the Devise `user` model:

```bash
rails g devise user
```

### 9. Add `user_id` to Friends Table

Create a migration to add the `user_id` column to the `friends` table:

```bash
rails g migration AddUserIdToFriends user_id:integer:index
```

Then run the migration:

```bash
rails db:migrate
```

### 10. Install and Update Bundles

Make sure all gems are installed and up to date by running:

```bash
bundle install
bundle update
```

### 11. Start the Rails Server

Finally, start the Rails server:

```bash
rails s
```

You can now visit the application in your browser at `http://localhost:3000`.

---

Now, you have a working Rails application with authentication (via Devise) and basic CRUD functionality for managing friends!
