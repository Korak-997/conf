# Live Reload For Rails Projects

* #### We need Guard-livereload gem
  For this we need to add **guard-livereload** gem to our Gemfile.
  We need to add the gem to **Development Group** , because we need it only in Development
  ```
  group :development do
    gem 'guard-livereload', '~> 2.5', require: false
  end
  ```
  Then in the terminal write :
  ```
  $ bundle install
  ```
  This command will download and configure all needed **Configs**
* Now in the Terminal write :
  ```
  $ bundle exec guard init livereload
  ```
  This command will add Guardfile to the project.
* We also need **rack-livereload** gem. We will add   it in **Development Group** also.
  ```
  group :development do
    gem 'guard-livereload', '~> 2.5', require: false
    gem 'rack-livereload'
  end
  ```
  Then in the terminal write :
  ```
  $ bundle install
  ```
  This command will download and configure all needed **Configs**.
* Now we need to add the **middleware** to our **Rails middleware** stack
  For this open **config/environments/development.rb**
  Add the code below to the end of the file
  ```
  # Add Rack::LiveReload to the bottom of the middleware stack with the default options:
  config.middleware.insert_after ActionDispatch::Static, Rack::LiveReload
  ```

We are all set now all we need is running the rails Server again with :

```
$ rails s
```

and in a new tab of the **terminal** run :

```
$ bundle exec guard
```

**Now enjoy Developing while your browser refreshes after any change**

-----------------------------------

## Note:
If you had any Issues that the changes in **scss** files are not watched.
Add this line :
```
 # file needing a full reload of the page anyway
  watch(%r{app/assets/stylesheets/.+\.scss})
```
To the **Guardfile**
