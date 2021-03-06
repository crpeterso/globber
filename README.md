# Globber
Utilize the ruby on rails environment backed by any remote API!

[![Gem Version](https://badge.fury.io/rb/globber.svg)](http://badge.fury.io/rb/globber)

## Installation
In your `Gemfile`:
```ruby
gem 'globber'
```
## Setup options:

### Automagically
- Run `rails g globber:install` in the root directory of your project
- Open `config/initializers/globber.rb` and set your `base_uri`

![Jake & Fin](http://img2.wikia.nocookie.net/__cb20120315182857/adventuretimewithfinnandjake/images/7/72/S2e13_FinnMagicWand.gif)

### Manually (not as magical)
In `config/routes.rb`:
```ruby
mount Globber::Engine => "/"
```
In `config/initializers/globber.rb`:
```ruby
Globber.configure do |c|
  c.base_uri = 'http://api.yoursite.com'
end
```
----
Now whichever route is passed to rails will be mapped to your API server.

That's it!

## Author
[@jakenberg](https://github.com/jakenberg)