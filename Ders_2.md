# Day_17 Boolean, Operators, Date
**Boolean dəyərlər**
```js
let isLightOn = true
let isRaining = false
let isHungry = false
let isMarried = true
let truValue = 4 > 3    // true
let falseValue = 4 < 3  // false
```
**True ve false dəyərlər**
*	***True dəyərlər***
	* Bütün müsbət və mənfi ədədlər (sıfırdan başqa)
	* Bütün string tipində olan yazılar ( "" - boş stringdən başqa )
	* Bolean dəyəri - true
* ***False dəyərlər***
	* 0 - sıfır
	* null
	* undefined
	* NaN
	* ( "" , '' ) boş string
	* Bolean dəyəri - false

## Operatorlar
**Arithmetic opratoru**
Arifmetik operatorlar **riyazi** operatorlardır.
* **( + )** -> ( x + y ) 
* **( - )** -> ( x - y ) 
* **( \* )** -> ( x * y )  
* **( / )** -> ( x / y ) 
* **( % )** -> ( x % y )
* **( \*\* )** -> ( x ** y ) 

```js
let number1 = 40
let number2 = 5
let result1 = number1 - number2
console.log(result1) // 35

let number3 = 4
let number4 = 16
let result2 = number3 * number4
console.log(result2) // 64
```
\
**Asigment opratoru**
JavaScript-də bərabər **Asign** operatorudur. Dəyişən təyin etmək üçün istifadə edir.
* **( = )** ( x=y ) -> x = y
* **( += )** -> ( x += y ) ->  x = x + y 
* **( -= )** -> ( x -= y ) ->  x = x - y 
* **( \*= )** -> ( x *= y ) ->  x = x * y 
* **( /= )** -> ( x /= y ) ->  x = x / y 
* **( %= )** -> ( x %= y ) ->  x = x % y
* **( \**= )** -> ( x **= y ) ->  x = x ** y 

```js
let num1 = 5
let num2 = 10
num1 += num2	// num1 = num1 + num2 
console.log(num1) // 15

let num3 = 40
let num4 = 10
num3 /= num4	// num3 = num3 / num4 
console.log(num3) // 4
```
\
**Comparison operatoru**
Proqramlaşdırmada biz dəyərləri müqayisə edirik, iki dəyəri müqayisə etmək üçün müqayisə **( comparison )** operatorlarından istifadə edirik.
* **( x == y )** -> x , y - ə bərabərdir
* **( x === y )** -> x , y - ə tam bərabərdir. ( tipləri də!)
* **( x != y )** -> x , y - ə bərabər deyil.
* **( x > y )** -> x , y - dən böyükdür.
* **( x < y )** -> x , y - dən kiçikdir.
* **( x >= y )** -> x , y - dən böyük bərabərdir.
* **( x <= y )** -> x , y - dən kiçik bərabərdir.

```js
console.log(3 > 2)              // true, (çünki 3, 2-dən böyükdür)
console.log(3 >= 2)             // true, (çünki 3, 2-dən böyük bərabərdir)
console.log(3 < 2)              // false,(çünki 3, 2-dən kiçik deyil)
console.log(2 < 3)              // true, (çünki 2, 3-dən kiçikdir)
console.log(2 <= 3)             // true, (çünki 2, 3-dən kiçik bərabərdir)
console.log(3 == 2)             // false, (çünki 3, 2-yə bərabər deyil)
console.log(3 != 2)             // true, (çünki 3, 2-yə bərabər deyil)
console.log(3 == '3')           // true, (çünki 3, 3-ə bərabərdir)
console.log(3 === '3')          // false,(3, 3-ə bərabərdir amma tipləri eyni deyil)
console.log(3 !== '3')          // true, (3, 3-ə bərabərdir amma tipləri eyni deyil)
console.log(3 != 3)             // false, (çünki 3, 3-ə bərabər deyil)
console.log(3 !== 3)            // false, (çünki 3, 3-ə bərabərdir və tipləri də eynidir)
console.log(0 == false)         // true, (ikisi də false dəyərlərdir)
console.log(0 === false)        // false,(ikisi də false dəyərlərdir amma tipləri eyni deyil)
console.log(1 == true)          // true, (ikisidə true dəyərlərdir)
console.log(1 === true)         // false,(ikisi də true dəyərlərdir amma tipləri eyni deyil)

console.log(undefined == null)  // true (ikisi də false dəyərlərdir)
console.log(undefined === null) // false (ikisi də false dəyərlərdir amma tipləri eyni deyil)


console.log('mango'.length == 'avocado'.length)  // false
console.log('mango'.length != 'avocado'.length)  // true
console.log('mango'.length < 'avocado'.length)   // true
console.log('milk'.length == 'meat'.length)      // true
console.log('milk'.length != 'meat'.length)      // false
console.log('tomato'.length == 'potato'.length)  // true
console.log('python'.length > 'dragon'.length)   // false
```
\
**Logical operatoru**
* **&&** - ( **AND** operatoru ) **hər iki tərəfin ( true )** olduğu halda true olur.  Digər hallarda ( false )
* **| |** - ( **OR** operatoru ) nəticənin true olması üçün **bir tərəfin true** olması kifayətdir.
* **!** - ( **NOT** operatoru ) bool dəyərini əksinə çevirər.  True dəyəri False, False dəyəri True edər.

```js
// && ampersand operator example

const check1 = 4 > 3 && 10 > 5		  // true && true -> true
const check2 = 4 > 3 && 10 < 5         // true && false -> false
const check3 = 4 < 3 && 10 < 5         // false && false -> false

// || pipe or operator, example

const check4 = 4 > 3 || 10 > 5         // true  || true -> true
const check5 = 4 > 3 || 10 < 5         // true  || false -> true
const check6 = 4 < 3 || 10 < 5         // false || false -> false

//! Negation examples

let check7 = 4 > 3                     // true
let check8 = !(4 > 3)                  // true -> false
let isLightOn = true
let isLightOff = !isLightOn           // true -> false
let isMarried = !false                // false -> true
```
\
**Increment operatoru(++)**
Dəyişəndə ​​saxlanılan dəyəri 1 vahid artırmaq üçün **Increment** (artım) operatorundan istifadə edirik.  Gəlin onların hər birinə baxaq:

* **Pre-increment**
	```js
	let count = 0
	console.log(++count) // count = 1 , Həmin sətirdə dəyər 1 vahid artır
	console.log(count)   // 1
	```
* **Post-increment**
	```js
	let count = 0
	console.log(count++) // count = 0 , Növbəti sətirdə dəyər 1 vahid artır	
	console.log(count)   // 1
	```
\
\
**Decrement operatoru(- -)**
Dəyişəndə ​​saxlanılan dəyəri 1 vahid azaltmaq üçün **Decrement** (azalma) operatorundan istifadə edirik.  Gəlin onların hər birinə baxaq:

* **Pre-increment**
	```js
	let count = 0
	console.log(--count) // count = -1, Həmin sətirdə dəyər 1 vahid azalır
	
	console.log(count)   // -1
	```
* **Post-increment**
	```js
	let count = 0
	console.log(count--) // count = 0 , Növbəti sətirdə dəyər 1 vahid azalır
	console.log(count)   // -1
	```
\
\
**Ternary operatoru**
Ternary operator şərti yazmağa imkan verir. Şərti yazmağın başqa bir yolu Ternary operatorlardan istifadə etməkdir.
```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
  
// Console: You need a rain coat.


number = -11
number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
  
// Console: -11 is a negative number
```


## ## Window Methods
**Window alert() method**
Adından da gördüyünüz kimi alert() metodu müəyyən mesaj və OK düyməsi olan xəbərdarlıq qutusunu göstərir.
```js
let message = 'JavaScript'
alert(message)
alert('Welcome to 30DaysOfJavaScript')
```

**Window prompt() method**
prompt() metodu, giriş dəyərlərini qəbul etmək üçün brauzerinizdə girişi olan sorğu qutusunu göstərir və daxil etdiyiniz məlumatı bir dəyişənə mənimsədir. prompt() metodu iki arqument alır. İkinci arqument istəyə bağlıdır.
```js
let number = prompt('Enter number', 'number goes here')
alert(number)
```
**Window confirm() method**
  
confirm() metodu OK və Cancel (ləğv) düyməsi ilə birlikdə müəyyən mesajı olan dialoq qutusunu göstərir. Təsdiq qutusu istifadəçidən nəyisə yerinə yetirəndə icazə almaq üçün istifadə olunur. confirm() arqument kimi string qəbul edir. OK düyməsini sıxmaq **true** dəyər verir, Cancel düyməsini sıxmaq isə **false** dəyər verir.
```js
const agree = confirm('Are you sure you like to delete? ')
console.log(agree) 
// Sizin seçiminizdən asılı olaraq true və ya false olur
```

## Date obyekti
Zaman vacib bir şeydir. Müəyyən bir fəaliyyətin və ya hadisənin vaxtını bilmək istəyirik. JavaScript-də cari vaxt və tarix **Date** obyekti istifadə edərək qurulur. Date obyektinin özünəməxsus metodları vardır.

**Creating a time object**
```js
const now = new Date()
console.log(now) 
```
Biz vaxt obyekti qurmuşuq və qeyd etdiyimiz **get** metodlarından istifadə edərək obyektdən istənilən tarix-saat məlumatını əldə edə bilirik.

* **getFullYear()**
	```js
	const now = new Date()
	console.log(now.getFullYear()) // 2022
	```
* **getMonth()**
	```js
	const now = new Date()
	console.log(now.getMonth()) 
	// Aylar sıfırdan başlayır(0-11). Yavar 0, Dekabr 11-dir.
	```
* **getDate()**
	```js
	const now = new Date()
	console.log(now.getDate()) // 8, çünki ayın 8-idir, gün(1-31)
	```
* **getDay()**
	```js
	const now = new Date()
	console.log(now.getDay()) // 2
	```
* **getHours()**
	```js
	const now = new Date()
	console.log(now.getHours())  // 0, çünki saat  00:56:41
	```
* **getMinutes()**
	```js
	const now = new Date()
	console.log(now.getMinutes())  // 56, çünki saat  00:56:41
	```
* **### seconds()**
	```js
	const now = new Date()
	console.log(now.seconds()) // 41, çünki saat 00:56:41
	```
* **_getTime_()**
	```js
	const now = new Date() //
	console.log(now.getTime())
	```


Hazırladı - **Zahid Vahabzadə** 

Video dərslər üçün Youtube kanalım - **[Biraz Kod Yazaq](https://www.youtube.com/channel/UCRlKqhooswsmfkxnokxcB0g)** 

Javascript-dən digər dokumentlər üçün - **[Github kanalım](https://github.com/Zahidoz/Javascript_Tedris)**
