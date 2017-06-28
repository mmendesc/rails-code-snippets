**Gemfile**

```ruby
gem 'figaro'
```


**In the console**

```
bundle exec figaro install
```


**set key**

```yaml
# config/application.yml

production:
  devise_secret_key: 'xxxxxx'
```

**using the key**

```ruby

#config/initializer/devise.rb

config.secret_key = Figaro.env.devise_secret_key

```

**Set secret in heroku**

```
figaro heroku:set -e production
```
