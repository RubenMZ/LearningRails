# Ruby on Rails Tutorial sample application

This is the sample application for
[*Ruby on Rails Tutorial:
Learn Web Development with Rails*](http://www.railstutorial.org/)
by [Michael Hartl](http://www.michaelhartl.com/).

## License

All source code in the [Ruby on Rails Tutorial](http://railstutorial.org/)
is available jointly under the MIT License and the Beerware License. See
[LICENSE.md](LICENSE.md) for details.

## Getting started

To get started with the app, clone the repo and then install the needed gems:

```
$ bundle install --without production
```

Next, migrate the database:

```
$ rails db:migrate
```

Finally, run the test suite to verify that everything is working correctly:

```
$ rails test
```

If the test suite passes, you'll be ready to run the app in a local server:

```
$ rails server
```

To generate and destroy controllers/models, and migrate DB / undo migrate.

``
$ rails generate controller StaticPages home help
$ rails destroy  controller StaticPages home help
$ rails generate model User name:string email:string
$ rails destroy model User
---
$ rails db:migrate
$ rails db:rollback
$ rails db:migrate VERSION=0
```

For more information, see the
[*Ruby on Rails Tutorial* book](http://www.railstutorial.org/book).