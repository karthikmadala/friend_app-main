# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version 3.3.7 And Rails version 8.0.1

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

**Steps to build this APP**
*
* Step1: bundle install

* Step2: rails g controller home index

* Step3: rails g scaffold Friend first_name:string last_name:string email:string:uniq phone:string:uniq

* step4: add "gem devise" in Gemfile

* Step5: bundle install

* step6: rails g devise:install
  *follow after this

  * add deveploment file code which is shown in terminal
 
  * set root path like root "home#index"
 
  * rails g devise:views
 
* rails db:migrate

* rails g devise user

* rails g migration AddUserIdToFriends userid:integer:index

* rails g migrate

* bundle install and bundle update

* rails s

  
# friends_app-using-rails 
