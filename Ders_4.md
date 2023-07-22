# Loops (Dövr)
Həyatda etdiyimiz fəaliyyətlərin əksəriyyəti təkrarlarla doludur. Təsəvvür edin ki, sizdən console.log() istifadə edərək **0-dan 100-ə qədər** çap etməyi xahiş etsəm, bu sadə tapşırığı yerinə yetirmək 5-6 dəqiqə çəkə bilər, bu cür yorucu və təkrarlanan tapşırıqlar dövr istifadə etməklə daha asan həyata keçirilə bilər.

  
Proqramlaşdırma dillərində təkrarlanan tapşırıqları yerinə yetirmək üçün müxtəlif növ dövr operatorlarından istifadə edirik. Aşağıdakı nümunələr JavaScript və digər proqramlaşdırma dillərində çox istifadə olunan dövr operatorlarıdır.

### for - dövr operatoru
for dövr operatoru **işələmə prinsipi** ->  Aşağıdakı sintaksisə fikir versəniz. for bloku içərisində **başlanğıc dəyərimiz** var və əgər şərt **true** olarsa blok icra olunacaq. Amma növbəti yoxlanışda dəyişənin(indeksin) dəyəri increment və ya decrement ilə **dəyişə bilər**. (növbəti index-ə keçmək üçün)

```js
// For loop structure
for(başlanğıc dəyər, şərt, increment/decrement){
  // şərt true olanda kod bloku icra edilir
}
```
\
Gəlin 1-dən 5-ə qədər ədədləri console-a çap edək.
Aşağıdakı misalda **başlanğıc dəyər sıfırdır ( i = 0 )**, 
və sıfır 5-dən kiçik olduğu üçün **true ( i <= 5 )** olur və blok icra olunur. 
Amma unutmayaq ki dəyərin sonrakı dövrdə qiyməti **1 vahid artacaq ( i++ )**
Bu dövr şərt **false olanadək** davam edir.
```js
for(let i = 0; i <= 5; i++){
  console.log(i)
}
// 0 1 2 3 4 5
```
Bu misalda isə 5 dən 0-a qədər ədədləri çap edək.
```js
for(let i = 5; i >= 0; i--){
  console.log(i)
}
// 5 4 3 2 1 0
```
Sıfırdan 5-ə qədər olan ədədləri öz-özünə vurub interpolasiya ilə ekrana çıxardaq.
```js
for(let i = 0; i <= 5; i++){
  console.log(`${i} * ${i} = ${i * i}`)
}
// 0 * 0 = 0
// 1 * 1 = 1
// 2 * 2 = 4
// 3 * 3 = 9
// 4 * 4 = 16
// 5 * 5 = 25
```
\

Aşağıdakı misalda şəhər adları olan bir array var. Əgər bizə bütün hərflərini böyük etməyimizi istəsəydilər bunun üçün **1)** Yeni bir boş newArr qururuq. **2)** countries array-ində olan şəhər adlarını böyük hərflərə çevirib, **3)** newArr-ə mənimsədirik (bərabər edirik)
```js
const countries = ['Finland', 'Sweden', 'Denmark', 'Norway', 'Iceland']
const newArr = []
for(let i = 0; i < countries.length; i++){
  newArr.push(countries[i].toUpperCase())
}

// ["FINLAND", "SWEDEN", "DENMARK", "NORWAY", "ICELAND"]
```
Array-dəki bütün ədədlərin cəmini tapmaq istəsək **Sum** dəyişəni qurub, hər dövrdə indeksin dəyərini sum dəyişəninə əlavə edirik. Bunun üçün sum dəyişəninə başlanğıc qiyməti sıfır veririk.
```js
const numbers = [1, 2, 3, 4, 5]
let sum = 0
for(let i = 0; i < numbers.length; i++){
  sum  = sum + numbers[i]  // can be shorten, sum += numbers[i]

}

console.log(sum)  // 15
```
Array-dəki ədədlərin kvadratını tapıp yeni bir array-ə mənimsətmək istəsək...
```js
const numbers = [1, 2, 3, 4, 5]
const newArr = []
let sum = 0
for(let i = 0; i < numbers.length; i++){
  newArr.push( numbers[i] ** 2)

}

console.log(newArr)  // [1, 4, 9, 16, 25]
```

## While - dövr operatoru
**for** - operatoru əsasən array üzərində əməliyyatlar apararkən  istifadə olunur.
**while** - operatoru isə müəyyən bir şərtə əsasən dövr edir
Gəlin sintaksisə baxaq: For operatorundakı kimi başlanğıc dəyərimiz olur. Və şərt false olanadək while dövrü təkrarlanır.
Ədədləri 0-dan 5-ə qədər console-a çap edək.
```js
let i = 0
while (i <= 5) {
  console.log(i)
  i++
}

// 0 1 2 3 4 5
```
\
Bəs **do while** nədir?  
şərtin true vəya false olmasına baxmayaraq heç olmasa dövrün azı bir dəfə icra olmağını istəyiriksə **do while** istifadə edilir.
```js
let i = 0
do {
  console.log(i)
  i++
} while (i <= 5)

// 0 1 2 3 4 5
```
Aşağıdakı misalda da gördüyünüz kimi while şərti false olsa belə dövr bir dəfə icra olunur.
```js
let i = 6
do {
  console.log(i)
  i++
} while (i <= 5)

// 6
```
\
## for of
Massivlər üçün for of loop istifadə edirik. Əgər biz massivdəki hər bir elementin indeksi ilə maraqlanmırıqsa, bu, ən qısa üsuludur.
Gəlin sintaksisə baxaq:
```js
for (const element of array) {
  // icra olunan kod bloku
}
```
\
Əvvəli misalı bir də bu formada yazaq.
```js
const numbers = [1, 2, 3, 4, 5]

for (const num of numbers) {
  console.log(num)
}
// 1 2 3 4 5
```
Ədədləri öz-özünə vurmaq istəsək...
```js
for (const num of numbers) {
  console.log(num * num)
}
// 1 4 9 16 25
```
Array-dəki sözlərin hərflərini böyük etmək istəsək...
```js
const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
]

for (const tech of webTechs) {
  console.log(tech.toUpperCase())
}
// HTML CSS JAVASCRIPT REACT NODE MONGODB
```

## break
Break aid olduğu **dövrü kəsmək** üçün istifadə olunur.
Aşağıdakı misalda **i == 3** olduqda dövr dayanır.
```js
for(let i = 0; i <= 5; i++){
  if(i == 3){
    break
  }
  console.log(i)
}

// 0 1 2
```

Hazırladı - **Zahid Vahabzadə** 
Video dərslər üçün Youtube kanalım - **[Biraz Kod Yazaq](https://www.youtube.com/channel/UCRlKqhooswsmfkxnokxcB0g)** 
Javascript-dən digər dokumentlər üçün - **[Github kanalım](https://github.com/Zahidoz/Javascript_Tedris)**
