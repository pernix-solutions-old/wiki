# Rubocop

#### 0. Add the gems
Add the following gems to the `Gemfile`
```ruby
#...
group :development, :test do
  # ...
  gem "rubocop", require: false
  gem "rubocop-rspec"
  #...
end
#...
```

#### 1. Install the gems
```shell
$ bundle install
```

#### 2. Add base configuration file
Copy our base configuration from [here](https://gist.github.com/pernix-dev/bd87e002a3781bcc620aa77b014951ce) to a new file `.rubocop-pernix.yml`.

That will include all the rules that we think every project should conform to. If you think a rule should be added/modified/deleted please notify @captain_macho in Slack.

#### 2. Add project configuration file
Create a new file `.rubocop.yml` that has the following content
```yml
require: rubocop-rspec

inherit_from:
  - .rubocop-pernix.yml
```