# Image_tag
```ruby
image_tag("icon.png", size: "16x10", alt: "Edit Entry")
image_tag("/icons/icon.gif", size: "16")
```
# Display html tag
```ruby
# show the raw html tag
<% @lists.each do |list| %>
	<%=raw list.name %>
<% end %>
```
```ruby
list.name.html_safe # perform the html tag
strip_tags() # strip the html tag
```
# Pagination(gem:kaminari)
```ruby
# gemfile
gem 'kaminari'
```
```ruby
# controller
@events = Event.page(params[:page]).per(5)
```
```ruby
# view
<%= paginate @events %>
```
[Reference](https://github.com/kaminari/kaminari)
# Authentication(gem:devise)
```ruby
# gemfile
gem 'devise' 
```
```ruby
# terminal
rails g devise:install
rails g devise user
rake db:migrate
rails g devise:views
```
### Authentication
```ruby
# controller
before_action :authenticate_user!, only: [:new, :edit, :create, :update, :destroy] 
```
```ruby
# strong_parameters
# controller
before_filter :configure_permitted_parameters, if: :devise_controller?

protected
  def configure_permitted_parameters
  devise_parameter_sanitizer.for(:sign_up) { |u| u.permit(:name, :email, :password,:password_confirmation) } 
end
```
### Attachment(gem:paperclip)
[Reference](https://github.com/thoughtbot/paperclip)
