# String 
```javascript
const a = 'cat'.charAt(1)   //  'a'
const b = 'cat'[1]   // 'a'
//Length
const aStringLength = aString.length //12

//toUpperCase & toLowerCase
const aString = 'Hello World!'
const bString = aString.toUpperCase()
const cString = aString.toLowerCase()

//trim
const bString = aString.trim()

//indexOf
console.log( aString.indexOf('Apple') ) // 0
console.log( aString.indexOf('Mongo') ) // 6
console.log( aString.indexOf('Banana') ) // 12
console.log( aString.indexOf('Honey') ) // -1

//substring
const aString = '0123456789'
console.log(aString.substring(0, 3)) //012
console.log(aString.substring(5, 8)) //567
```
# Template strings
```javascript
const a = ` I 
am
Tom`
const name = 'Tom'
console.log(`Hello ${firstName}!`)
```
# Escape characters
```javascript
const aString = 'It\'s ok'
const bString = 'This is a blackslash \\'
```
# Float to Integer
```javascript
const floatValue = 10.55
const intValueOne = Math.floor( floatValue ) 
const intValueTwo = Math.ceil( floatValue )
const intValueThree = Math.round( floatValue )
```
# carry
```javascript
// Binary starts with 0b or 0B
const FLT_SIGNBIT  = 0b10000000000000000000000000000000 // 2147483648
//Octal starts with 0o or 0O
const n = 0O755 // 493
//Hexadecimal starts with 0x
const x = 0xFF
```
# Number
```javascript
//to Decimal
const binaryNumber = Number('0b11') // 3
```
# toString
```javascript
// toString(radix)
console.log(decimalNumber.toString(2)) //'1111101'
```
# parseInt
```javscript
// parseInt(String, radix)
const octalNumber = parseInt('071', 8)
```
# parseFloat
```javascript
//String to Float
const cNumber = parseFloat("10.33") //10.33
```
# typeof
```javascript
typeof 10
typeof 10.4
```
# output
```javascript
console.log('Hello') // can't perform on IE 6, 7
alert('Hello') // show messagebox
document.write('Hello') // override whole page 
```
# undefine & null
```javascript
var a; # udefine
var a = null; #null
```
# alert & prompt
```javascript
var msg = "hello world";
alert(msg);
var input = prompt("what is your name?");
```
# Dom selector
```javascript
//querySelector: first element

//querySelectorAll: all the element

//getElementById
document.getElementById("demo").innerHTML = 'Hello'
//getElementsByClassName
var tags = document.getElementsByClassName("bolded");
//getElementsByTagName
var tags =document.getElementsByTagName("h1"); 
```
# textContent
```javascirpt
var myHeading = document.querySelector('h1');
myHeading.textContent;
```
# innerHTML
```javascript
var myHeading = document.querySelector('h1');
myHeading.innerHTML = 'Hello World';
```
# getAttribute & setAttribute
```javascript
var a = document.querySelector("a");
a.getAttribute("href");
setAttribute("href", "www.google.com");
```
# addEventListner
[reference](https://developer.mozilla.org/zh-TW/docs/Web/Events)

```javascript
tag.addEventListner("click", func_name)
```
# onclick
```javascript
document.querySelector('button').onclick = function(){
	alert('hey ');
}
```
# localStorage 
```javascript
localStorage.setItem('name', myName);
var storedName = localStorage.getItem('name');
```
# MATH
```javscript
// starts from 1, 1-6
console.log(Math.floor(Math.random() * 6) + 1
```
# AJAX
```javascript
$.ajax({
    url: './sample.json',
    data: {
        id: 'a001'
    },
    type: 'GET',
    dataType : 'json',
})
```
