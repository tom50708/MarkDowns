#Basic
```ruby
user_input = gets.chomp # user input
user_input.upcase! #change all to upper case
user_input.downcase! #change all to lower case
user_inpt.capitalize! #change the first character to upper case 
user_input.gsub!(exp, str)  #replace
user_input.include? "str" #included or not
user_input.to_s # to String
user_input.to_i # to Integer
user_input.to_sym  # to Symbol
user_input.intern  # to Symbol
user_input.floor # round
user_input.nil? # check nill or not, return boolean
```
#if
```ruby
if a ==0
    puts "zero"
elsif a==10
    puts "ten"
else
    puts "non zero & ten"
end
```
#unless
```ruby
unless false
    puts "F"
else
    puts "T"
end
```
#while
```ruby
while i <0
    i+=1
end
```
#until
```ruby
until i >0 
    i+=1
end
```
#loop do
```ruby
i = 20
loop do
    i-=1
    next if i % 2 == 1 # continue in java
    print "#{i}"
    break if i <= 0
end
```
#for
```ruby
for num in 1..10
    puts "#{num}"
end
```
#Range
```ruby
1...10 # print 1-9 
1..10 # print 1-10
```
#times
```ruby
10.times {print "time"}
```
#each
```ruby
multi_d_array.each { |x| puts "#{x}\n" } # Array
family.each { |x, y| puts "#{x}: #{y}" } # Hash & Array

multi_d_array.each do |x| 
    puts "#{x}\n" 
end
```
#split & join
```ruby
# array chagne to string, it looks like 1:2:3 
str = ary.join(":") 
# string change to array, it looks like ["1", "2", "3"]
str.split(":") 
```
#Array
```ruby
arr = []
arr = [1, 2 ,3 ,4] # numbric array
arr = ["1", "2", "3`, "4"] # string array
arr = [1, "2", 3, "4"] # alow to mix 
arr = [[0, 0][0, 0]] # 2D array
```
#Hash
```ruby
my_hash = Hash.new
my_hash = Hash.new(0) # set default value
my_hash = {}
pets["pet"] = "cat" # add key:pet value:cat
pets = {
    "tank" => "cow",
    "dps_1" => "tom",
    "dps_2" => "amy",
    "dps_3" => "john",
}
my_hash.each_key { |k| print k, " " } # only key
my_hash.each_value { |v| print v, " " } # only value
```
#Method
```ruby
def my_method(arg, *args)
    args.each {|a| puts "#{arg}, #{a}" }
end
my_method("hi", "tom", "john", "amy")
```
#Sort
```ruby
a = [ "d", "a", "e", "c", "b" ]
my_array.sort! # string, in
a = my_array.sort
a.sort!                   # ["a", "b", "c", "d", "e"] ASC
a.sort!.reverse      # DESC
a.sort { |x,y| y <=> x }  # ["e", "d", "c", "b", "a"]  DESC
a.sort { |x,y| x <=> Y }  # ["a", "b", "c", "d", "e"] ASC
```
#combined comparison operator
```ruby
# return 0 are the same
# return 1 first one greater than second one
# return -1 first one less than second one
book_1 <=> book_2 
```
#Select
```ruby
a = grades.select {|name, grade| grade < 97}
a = grades.select { |k, v| k == :alice }
```
#Ternary
```ruby
true ? "true" : "false"
```
#case when
```ruby
case language
when "JS"
  puts "Websites!"
when "Python"
  puts "Science!"
when "Ruby"
  puts "Web apps!"
else
  puts "I don`t know!"
end
```
Conditional assignment
```ruby
a = nil # puts nil
a ||= "hello" # puts hello
a ||= "hey" # puts hello
a = "hey" # puts hey
```
#upto & downto
```ruby
1.upto(100){|num| puts "#{num}"} # for numberic
"Z".downto("A"){|ch| puts "#{ch}"} # for string
```
#respond_to?
```ruby
# recognize the Object`s method 
# If it is. return true. If it isn`t. return false 
1.respond_to?(:next)
[1, 2, 3].respond_to?(:push) 
```
#Shortcut
```ruby
   one: "1"  # same as :one => "1"
    [1, 2, 3, 4] << 5 # same as push
    "abcd" << e # same as +=
```
#collect
```ruby
numbers=[1, 2, 3, 4]
numbers.collect{|num| num*2 }
numbers.collect!{|num| num*2 }
```
#yield
```ruby
#Example 01
def welcome(name)
    puts "welcom, #{name}"
    yield
    puts "To the RuRu land~"
end
welcome(name){puts" This is yield "}

#Example 02
def yield_name(name)
    puts "In the method! Let`s yield."
    yield("Kim")
    puts "In between the yields!"
    yield(name)
    puts "Block complete! Back in the method."
end

yield_name("Eric") { |n| puts "My name is #{n}." }
```
#Procs
```ruby
cube = Proc.new { |x| x ** 3 }
[1, 2, 3].collect!(&cube)
[4, 5, 6].map!(&cube)

hi = Proc.new { puts "Hello!" }
hi.call 

numbers_array = [1, 2, 3, 4, 5, 6, 7, 8, 9] # change num to string 
strings_array = numbers_array.collect(&:to_s)
```
#lambda
```ruby
strings = ["leonardo", "donatello", "raphael", "michaelangelo"]
symbolize = lambda{|s| s.to_sym }
symbols = strings.collect(&symbolize)

hi = lambda { puts "Hello!" }
hi.call 

symbol_filter = lambda{|p| p.is_a? Symbol}
symbols = my_array.select(&symbol_filter)
```
#Variable 
```ruby
name # local variable
@name # instance variable
@@name # class variable
$name # global variable
```
#Usage of Class Method
```ruby
class Papa
    def Papa.cook # or self.cook
        @@food = "omelette"
    end
end
Papa.cook # directly, use cook method in Papa, return "omelette"
```
#OOP
```ruby
# result => "pasta"
class Papa
    def cook
        puts "omelette"
    end
end

class Son < Papa #Son Inherits Papa
    def cook
        puts "pasta"
    end
end 
```
#Override & super
```ruby
# result => "pasta"
#           "omelette"
class Papa
    def cook
        puts "omelette"
    end
end

class Son < Papa
    def cook
        puts "pasta"
        super # Papa cook method
    end
end 
```
#Exception handling
```ruby
begin
    #first
rescue
    #error
ensure 
    #always
end
```