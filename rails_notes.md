# HTTP Verb
get(read)
post(create)
patch(update)
put(update)
delete(delete)
# Active Record
table equals class
datas equals object
# Validate
```ruby
validates :email, presence: true
validates :name, length: { minimum: 2 }
validates :name, length: { maximum: 200 }
validates :legacy_code, format: { with: /\A[a-zA-Z]+\z/,
    message: "only allows letters" }
```
# rake
```ruby
rails db:rollback
```
```ruby
Orders.create(name: 'Tom', description: 'yoyoyo')
Orders.find(1)
Orders.find(1).update(name: 'new Tom')
Orders.find(1).destroy

order = Order.find(1)
# object order includes attr_accessor 
order.name # new Tom
order.description # yoyoyo
```
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
# Attachment(gem:paperclip)
[Reference](https://github.com/thoughtbot/paperclip)
# Many to Many
```ruby
doctor = Doctor.create(name: "Mary")
patient = Patient.create(name: "Sam")

john = Doctor.find(1)

john.patients << paitent
```
# gem:pry
```ruby
gem 'pry'
# in action
binding.pry
# type params to check the imformation of parameters
```
# json
```ruby
respond_to do |format|
    format.html { redirect_to @post }
    format.json { render :show, status: :ok, location: @post }
end
```
```ruby
# directly output json
render json: @posts
```
# gem:rest-client
```ruby
gem 'rest-client'
```
# Command Line
```ruby
rails g model user --no-test-framework
```
