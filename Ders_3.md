# Conditionals
Şərti ifadələr müxtəlif şərtlər əsasında qərar qəbul etmək üçün istifadə olunur.
Şərtlər aşağıdakı yollardan istifadə etməklə həyata keçirilə bilər:
 * if
 * if , else
 * if , elseif, else
 * switch
 * ternary operator

## if
if - şərt blokudur , şərtin doğru olub-olmadığını yoxlayır və true olarsa blok kodunu yerinə yetirir.
```js
if (condition) {
	// Burdakı kodlar condition true olduğu halda icra olunur.
}
```
\
**Misal :**
```js
let num = 3

if (num > 0) {
  console.log(`${num} is a positive number`)
}

//  3 is a positive number
```
Yuxarıdakı şərt nümunəsində  3,  0-dan böyükdür, ona görə də müsbət rəqəmdir. Şərt doğru idi və kod bloku icra olundu. Lakin şərt yanlışdırsa, heç bir nəticə görməyəcəyik.
```js
let isRaining = true

if (isRaining) {
  console.log('Remember to take your rain coat.')
}
```

Eyni şey ikinci şərtə də aiddir, əgər isRaining yanlışdırsa if bloku icra olunmayacaqdı və biz heç bir çıxış görməyəcik. False vəziyyətin nəticəsini görmək üçün başqa bir bloka sahib olmalıyıq.

## if, else
Şərt doğru olarsa, birinci blok yerinə yetiriləcək, əks halda başqa şərt yerinə yetiriləcək.
```js
// syntax
if (condition) {
  // condition trueolanda bu blok icra olunacaq
} 
else {
  // Heç bir şərt true olmayanda else bloku icra olunur
}
```
\
**Misal :**
```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
} 
else {
  console.log(`${num} is a negative number`)
}
//  3 is a positive number

num = -3
if (num > 0) {
  console.log(`${num} is a positive number`)
} 
else {
  console.log(`${num} is a negative number`)
}
//  -3 is a negative number
```
Son misalda **num=0**  olsaydı if bloku false olacaq deyə else bloku işləyəcək. Amma sıfır nə mübət nə də mənfi ədəddir. Bunun üçün **əlavə bir şərtə** ehtiyyac var.

## İf, Else if, Else
2 və daha artıq şərtdən istifadə ediriksə else if blokundan istifadə edirik.

```js
// syntax
if (condition) {
     // if blokunda şərt true olarsa icra olunur.
} 
else if (condition) { 
   // else if blokundakı şərt doğru olarsa icra olunur
} 
else {
    //  bütün şərtlər false olarsa icra olunur
}
```
\
**Misal :**
```js
let a = 0

if (a == 0) {
  console.log(`${a} is neither a positive nor a negative number`)
} 
else if (a < 0) {
  console.log(`${a} is a negative number`)
} 
else {
  console.log(`${a} is positive number`)
}
```
```js
let weather = 'sunny'

if (weather === 'rainy') {
  console.log('You need a rain coat.')
} else if (weather === 'cloudy') {
  console.log('It might be cold, you need a jacket.')
} else if (weather === 'sunny') {
  console.log('Go out freely.')
} else {
  console.log('No need for rain coat.')
}
```

# ! ! ! else if 
Yuxarıdakı misallarda **else if** yerinə **if** yaza bilərdik. Gəlin bir baxaq.
```js
let a = 0

if (a == 0) 
{ // {} if blokunun scope sahəsinin başlanğıcı
  console.log(`${a} is neither a positive nor a negative number`)
} // {} if blokunun scope sahəsinin sonu
if (a < 0) {
  console.log(`${a} is a negative number`)
} 
else {
  console.log(`${a} is positive number`)
}
```

Bəs bir-birilərindən **fərqləri** nədir?
**( if ) -> hər zaman**  şərti yoxlayır və şərt doğrudursa həmin blokun kodları icra olunur.
**( else if ) -> yuxarıdakı bütün şərtlər false olarkən** şərti yoxlayır və şərt doğrudursa həmin blokun kodları icra olunur.
**( else ) -> Yuxarıdakı heç bir şərt doğru olmadıqda**  icra olunur. Yalnız bir dəfə ən aşağıda yazılır. else blokunda şərt yazılmır.

## Switch
Switch if, else if, else üçün **alternativdir**. Switch bir açar sözündən sonra mötərizə və kod bloku ilə başlayır. Kod blokunun içərisində fərqli hallarımız olacaq. **case** bloku, mötərizəsindəki dəyər işin dəyərinə uyğun gəlirsə, işləyir. **break** bloku icranı dayandırmaq üçündür ki, şərt yerinə yetirildikdən sonra kodun icrası aşağı düşməsin. **default** blok, yuxarıdakı bütün hallar false olduqda işləyir, **else kimi :)**

```js
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```
\
**Misal :**
```js
let weather = 'cloudy'
switch (weather) {
  case 'rainy':
    console.log('You need a rain coat.')
    break
  case 'cloudy':
    console.log('It might be cold, you need a jacket.')
    break
  case 'sunny':
    console.log('Go out freely.')
    break
  default:
    console.log(' No need for rain coat.')
}
```
\
**Misal 2 :**
```js
switch (day) {
  case 'monday':
    console.log('Today is Monday')
    break
  case 'tuesday':
    console.log('Today is Tuesday')
    break
  case 'wednesday':
    console.log('Today is Wednesday')
    break
  case 'thursday':
    console.log('Today is Thursday')
    break
  case 'friday':
    console.log('Today is Friday')
    break
  case 'saturday':
    console.log('Today is Saturday')
    break
  case 'sunday':
    console.log('Today is Sunday')
    break
  default:
    console.log('It is not a week day.')
}
```
\
**Rəqəm daxil edək**
```js
let num = prompt('Enter number');
switch (true) {
  case num > 0:
    console.log('Number is positive');
    break;
  case num == 0:
    console.log('Numbers is zero');
    break;
  case num < 0:
    console.log('Number is negative');
    break;
  default:
    console.log('Entered value was not a number');
}
```

## Ternary Operators
Şərti yazmağın başqa bir yolu üçlü operatorlardan istifadə etməkdir. Biz bunu başqa əvvəlki dərslərdə izah etdik, lakin burada da qeyd etməliyik.
```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

Hazırladı - **Zahid Vahabzadə** 
Video dərslər üçün Youtube kanalım - **[Biraz Kod Yazaq](https://www.youtube.com/channel/UCRlKqhooswsmfkxnokxcB0g)** 
Javascript-dən digər dokumentlər üçün - **[Github kanalım](https://github.com/Zahidoz/Javascript_Tedris)**



