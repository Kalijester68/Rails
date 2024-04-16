         ___        ______     ____ _                 _  ___
        / \ \      / / ___|   / ___| | ___  _   _  __| |/ _ \
       / _ \ \ /\ / /\___ \  | |   | |/ _ \| | | |/ _` | (_) |
      / ___ \ V  V /  ___) | | |___| | (_) | |_| | (_| |\__, |
     /_/   \_\_/\_/  |____/   \____|_|\___/ \__,_|\__,_|  /_/
 -----------------------------------------------------------------


Hi there! Welcome to AWS Cloud9!

To get started, create some files, play with the terminal,
or visit https://docs.aws.amazon.com/console/cloud9/ for our documentation.

Happy coding!

rvm get stable
rvm install 3.1.2
rvm --default use 3.1.2

ruby -v
ruby 3.1.2p20 (2022-04-12 revision 4491bb740a) [x86_64-linux]

echo "gem: --no-document" >> ~/.gemrc

gem install rails -v 7.0.4

rails -v
Rails 7.0.4

gem install bundler -v 2.3.14

source <(curl -sL https://cdn.learnenough.com/resize)

rails _7.0.4_ new hello_app --skip-bundle

<-- Updated Gemfile -->
source "https://rubygems.org"
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby "3.1.2"

gem "rails",           "7.0.4"
gem "sprockets-rails", "3.4.2"
gem "importmap-rails", "1.1.0"
gem "turbo-rails",     "1.1.1"
gem "stimulus-rails",  "1.0.4"
gem "jbuilder",        "2.11.5"
gem "puma",            "5.6.4"
gem "bootsnap",        "1.12.0", require: false

group :development, :test do
  gem "sqlite3", "1.4.2"
  gem "debug",   "1.5.0", platforms: %i[ mri mingw x64_mingw ]
end

group :development do
  gem "web-console", "4.2.0"
end

group :test do
  gem "capybara",           "3.37.1"
  gem "selenium-webdriver", "4.2.0"
  gem "webdrivers",         "5.0.0"
end

group :production do
  gem "pg", "1.3.5"
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem.
# Uncomment the following line if you're running Rails
# on a native Windows system:
# gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]

cd hello_app/
bundle _2.3.14_ install

bundle install
bundle update


Listing 1.10: Allowing connections to the local web server.
config/environments/development.rb

Rails.application.configure do
  .
  .
  .
  # Allow connections to local server on cloud IDE.
  config.hosts.clear
end

rails server

Disable trackers if using firefox
Preview running application
Open site in new window

git --version
git version 2.40.1

git config --global user.name "Your Name"
git config --global user.email your.email@example.com
git config --global init.defaultBranch main
git config --global alias.co checkout
git config --global credential.helper "cache --timeout=86400"

cd ~/environment/hello_app
show hidden files and remove all .git files auto included by rails new
cd ../

git add -A
git status
git commit -m "Initialize repository"
git log

git remote add origin https://github.com/Kalijester68/Rails.git
git branch -M main
git push -u origin main

add .gitignore


