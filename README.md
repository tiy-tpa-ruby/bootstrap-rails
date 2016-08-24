# How to use Bootstrap with Scaffold and Rails

## Make a new rails app

`rails new bootstrap-rails`

## Go into the rails app directory

`cd bootstrap-rails`

## Edit the gemfile

`atom Gemfile`

## Add these gems:

```
gem 'haml-rails'
gem 'bootstrap-generators'
```

## Then bundle to update our gems

`bundle`

## Then we can install the bootstrap scaffold/templates

- For HAML with SCSS
  ```
  rails generate bootstrap:install --template-engine=haml

  /bin/rm app/views/layouts/application.html.erb
  ```

- For ERB with SCSS
  `rails generate bootstrap:install --stylesheet-engine=scss`

## Ensure SPRING is stopped to make sure rails changes are picked up

`spring stop`

## Now we can generate a scaffold for a model

`rails generate scaffold Term name definition author`

## Lets create our database, migration, and seed

`rake db:create db:migrate db:seed`

## Now we can launch the app and see nice bootstrap styling
