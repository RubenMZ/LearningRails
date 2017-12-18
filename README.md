# Ruby on Rails Tutorial

This is a tutorial to learn the basics of Rails : [Tutorial](https://www.railstutorial.org/book)

## How to install (on MacOSX)


### Installing Homebrew

```
ruby -e '$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)'
```

### Installing Ruby

```
brew install rbenv ruby-build
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile
$rbenv install 2.4.2
$rbenv global 2.4.2
$ruby -v
```

### Installing Rails

```
gem install rails -v 5.1.4
rbenv rehash
rails -v
# Rails 5.1.4
```

### Creating hello app

```
cd                  # Change to the home directory.
mkdir environment     # Make a environment directory.
cd environment/       # Change into the environment directory.
cd ~/environment
rails _5.1.2_ new hello_app
cd ~/environment/hello_app/
rails server
```

### Creating models

```
rails generate scaffold User name:string email:string
rails db:migrate
rails generate scaffold Micropost content:text user_id:integer
rails db:migrate
```

### Rails Console

```
rails console
>> first_user = User.first
=> #<User id: 1, name: "Michael Hartl", email: "michael@example.org",
created_at: "2016-05-15 02:01:31", updated_at: "2016-05-15 02:01:31">
>> first_user.microposts
=> [#<Micropost id: 1, content: "First micropost!", user_id: 1, created_at:
"2016-05-15 02:37:37", updated_at: "2016-05-15 02:37:37">, #<Micropost id: 2,
content: "Second micropost", user_id: 1, created_at: "2016-05-15 02:38:54",
updated_at: "2016-05-15 02:38:54">]
>> micropost = first_user.microposts.first    # Micropost.first would also work.
=> #<Micropost id: 1, content: "First micropost!", user_id: 1, created_at:
"2016-05-15 02:37:37", updated_at: "2016-05-15 02:37:37">
>> micropost.user
=> #<User id: 1, name: "Michael Hartl", email: "michael@example.org",
created_at: "2016-05-15 02:01:31", updated_at: "2016-05-15 02:01:31">
>> exit
```

### Generating a Static Pages controller

```
rails generate controller StaticPages home help
```

## License

*Ruby on Rails Tutorial: Learn Web Development with Rails. Copyright © 2016 by Michael Hartl. Last updated 2017/12/08 14:13:41 PT.*

*All source code in the Ruby on Rails Tutorial is available jointly under the MIT License and the Beerware License.*