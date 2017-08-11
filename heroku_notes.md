# installation
```
# mac
brew install heroku
# ubuntu 
wget -qO- https://cli-assets.heroku.com/install-ubuntu.sh | sh
```
# login
```
# terminal
heroku login
```
# production mode
```
# gemfile
group :production do
  gem 'pg'
end

# after that move gem 'sqlite3' to development instead 
```
# bundle install
```
# terminal
# automatically skips gem of production
bundle install --without production
```
# create
```
# terminal
git init
heroku create
```
# push 
```
git push heroku master
heroku run rake db:migrate
```
# open
```
heroku open
```
