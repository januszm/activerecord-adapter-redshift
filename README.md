activerecord-redshift-adapter
==============================

Amazon Redshift adapter for ActiveRecord 7+ (Rails 7+).
This is a fork from https://github.com/pennylane-hq/activerecord-adapter-redshift, which is a fork from
https://rubygems.org/gems/activerecord7-redshift-adapter hosted on a private Gitlab instance.
It's itself forked the project from https://github.com/kwent/activerecord6-redshift-adapter

Thanks to the auhors.

Usage
-------------------

For Rails, add the following in the Gemfile:

```ruby
gem 'activerecord-redshift-adapter'
```

Specify the adapter name in the `database.yml` file:

```YAML
development:
  adapter: redshift
  host: host
  port: port
  database: db
  username: user
  password: password
  encoding: utf8
```

or use it directly in the connection or `DATABASE_URL`:

```ruby
class SomeModel < ApplicationRecord
  establish_connection('redshift://username:password@host/database')
end
```

License
---------

MIT license (same as ActiveRecord)
