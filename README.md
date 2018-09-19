# Blog

A blog application where users can read or write articles. Admin role has the ability to edit/delete users as well as add article categories.

![blog](https://user-images.githubusercontent.com/15070059/45770764-4c937c00-bc11-11e8-961b-8a1d3afe14a4.png)

## Getting Started

### Installing

Make sure you have [Ruby](https://www.ruby-lang.org) and [Bundler](http://bundler.io) installed.

```sh
git@github.com:Vu-John/blog.git # or clone your own fork
cd blog
bundle install
rails db:migrate
```

Setup an admin user

```sh
rails console

 :001 > User.create(username:"admin", password:"password", admin: true)
 :001 > exit

rails s
```

Open up applicaiton http://localhost:3000

### Deploying to Heroku

Make sure you have [Heroku Toolbelt](https://toolbelt.heroku.com/) installed

```sh
heroku create <name_of_application>
git push heroku master
heroku run rails db:migrate
heroku open
```

Setup an admin user

```sh
heroku run rails console
User.create(username:"admin", password:"password", admin: true)
exit
```

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Built With

* [Ruby 2.3.3](https://www.ruby-lang.org/en/news/2016/11/21/ruby-2-3-3-released/)
* [Rails 5.1.4](https://rubygems.org/gems/rails/versions/5.1.4)
