# Data types


* **Primitiv** data tipləri 
	* **Number** - Integers ( tam ədədlər) , floats ( kəsr ədədlər ) 
	* **Strings** - Dırnaq içərisində məlumat ( ədəd, cümlə, simvollar)
	* **Booleans** - Doğru və ya yanlış ( true , false )
	* **Null** - Boş dəyər və ya dəyər yoxdur.
	* **Undefined** -  Dəyişənə dəyər vermədən bəyan etmək 
	* **Symbol** - Konstruktor tərəfindən qurulan unikal dəyər
* **Primitiv olmayan** data tipləri
	* **Object** - özünə xas məlumatları bir yerə yığır
	* **Array** -  oxşar tipli məlumatları bir yerə yığır

### Primitiv data tipləri
Primitiv data tipləri yalnız bir tipə aid olur.
```js
let num_1 = 12         // number
let num_2 = 8.6

let js = 'JavaScript'   // string
let name = 'IT Innovations'

let isLightOn = true 	// boolean
let isCorrect= false
```
### Primitiv olmayan data tipləri
Primitiv olmayan data tipləri fərqli tipdə olan məlumatları bir yerdə saxlaya bilir.
```js
let nums = [11, 5, 10] 	// Array
console.log(nums)  // [11, 5, 10]

let user = {  		 	// Object
	name:'Zahid',
	role:'Vahabzade',
	country:'Baku'
}
console.log(user.name , user.surname, user.country)
```

**Dəyişənlərin düzgün bəyan edilməsi**
```js
let age = 42		  // yaş sabir olmayan dəyişəndir  (  let  )
const gravity = 9.81  // gravity sabit dəyişəndir deyə ( const )
let weight = 72       // çəki dəyişə bilər
const PI = 3.14       // Riyaziyyatda PI sabit dəyişəndir

console.log(age, gravity, weight , PI)
```
### Math obyekti ( Riyazi obyekt)
```js
// PI sabit deyerdir. Hemise 3.14-e beraberdir
const PI = Math.PI 
console.log(PI)	 // 3.14

console.log(Math.round(9.81)) // yuvarlaqlaşdırar       ( 9 )
console.log(Math.round(PI))	  // PI = 3.14		  	    ( 3 )
console.log(Math.floor(PI))	  // asagi qiymeti goturer  ( 3 )
console.log(Math.ceil(PI))	  // yuksek qiymeti goturer ( 4 )

// Ededlerin içerisinden en kiçik qiymeti tapar
console.log(Math.min(3, 20, -7, 0, 11, -2))
// Ededlerin içerisinden en böyük qiymeti tapar
console.log(Math.max(3, 20, -7, 0, 11, -2))

const randNum = Math.random()
console.log(randNum) // 0 ile 1 arasında random eded verer

//Ekrana 1 ile 20 arasi random eded çıxartmaq istesek...
const num = Math.floor(Math.random () * 21)
console.log(num)

console.log(Math.abs(-25))	// musbet edede cevirer ( |-25| -> 25 )
console.log(Math.sqrt(81))  // kok altina salmaq ( 81 = 9 * 9 -> 9)
console.log(Math.pow(4, 3)) // quvvete yukseltme ( 4 ustu 3 -> 64)

Math.sin(0)
Math.sin(60)
Math.cos(0)
Math.cos(60)

```
**String**
```js
const firstName = 'Zahid'
const lastName = 'Vahabzade'
let fullName = firstName + ' ' + lastName;
console.log(fullName); // Zahid Vahabzade


console.log(`The sum of 2 and 3 is 5`)
let a = 2
let b = 3
// İnterpolasiya cümlə içərisində dəyişənin dəyərini göstərmək üçündür
console.log(`The sum of ${a} and ${b} is ${a + b}`)
```

**String Index**
```js
// index - 0 dan başlayır
// uzunluq - 1 den başlayır
let course= 'IT Innovations'
let anyLetter= course[1]  // T
let anyLetter= course[8]  // a
```

**toUpperCase() , toLowerCase()**
```js
let lessonName = 'JavaScript'
console.log(lessonName.toUpperCase()) // JAVASCRIPT

let lessonName = 'JavasScript'
console.log(lessonName.toLowerCase()) // javascript
```

**includes()**
```js
let string = '30 Days Of JavaScript'

console.log(string.includes('Days'))     // true
console.log(string.includes('days'))     // false
console.log(string.includes('Script'))   // true
console.log(string.includes('script'))   // false
console.log(string.includes('java'))     // false
console.log(string.includes('Java'))     // true
```


---
Hazırladı - **Zahid Vahabzadə** 

Video dərslər üçün Youtube kanalım - **[Biraz Kod Yazaq](https://www.youtube.com/channel/UCRlKqhooswsmfkxnokxcB0g)** 

Javascript-dən digər dokumentlər üçün - **[Github kanalım](https://github.com/Zahidoz/NodeJS_Tedris)**
