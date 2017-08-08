# installation
```
# terminal
brew install heroku
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
