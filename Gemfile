source "https://rubygems.org"
gemspec

DEFAULT_RAILS_VERSION = '6.0.3.5'
ENV['RAILS_VERSION'] ||= DEFAULT_RAILS_VERSION

if ENV['TARGET_DATABASE'] == 'postgresql'
  gem "pg"
else
  if ENV['RAILS_VERSION'] == '4.2.10'
    gem 'mysql2', '~> 0.3.18'
  else
    gem "mysql2"
  end
end

if ENV['RAILS_VERSION'] == 'master'
  gem "activerecord", git: "https://github.com/rails/rails"
else
  gem "rails", "~> #{ENV['RAILS_VERSION'] || DEFAULT_RAILS_VERSION}"
  gem "activerecord", "~> #{ENV['RAILS_VERSION'] || DEFAULT_RAILS_VERSION}"
end
