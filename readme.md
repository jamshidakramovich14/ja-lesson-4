
----- L O O P ----- /////////////////
FOR LOOP /////////
for (initializer; condition; iterator) {
  // statements
}

for (let i = 1; i <= 10; i++) {
  console.log(i);
}

for (let i = 2; i <= 10; i += 2) {
  console.log(i);
}

WITHOUT INITIALIZER ///
let j = 1; // initilizer
for (; j <= 10; j += 1) {
  console.log(j);
}

WITHOUT CONDITION ///
for (let j = 1; ; j += 1) {
  console.log(j);
  if (j > 10) {
    break;
  } // condition
}

WITHOUT ITERATOR ///
for (let j = 1; j <= 10; ) {
  console.log(j);
  j += 1; // iterator
}

WITHOUT ANY EXPRESSION ///
let j = 1; // initilizer
for (;;) {
  if (j <= 10) {
    console.log(j);
  } // condition
  j += 1; // iterator
}

WITHOUT LOOP BODY ///
for (let i = 0; i <= 10; i++, console.log(i));

for (let i = 1; i <= 10; i++) {
  console.log(i);
}

WHILE LOOP ///////////////
while (condition) {
  // code block to be executed
}

let i = 1;
while (i <= 10) {
  console.log(i);
  i++;
}

let count = 1;

while (count <= 10) {
  console.log(count);
  count += 1;
}

DO-WHILE LOOP ////
do {
  statement;
} while (condition);

let i = 11;
do {
  console.log(i);
  i++;
} while (i <= 10);

 SECRET NUMBER GAME //////////////////////////////////////
generate a secret number between 1 and 10
const MIN = 1;
const MAX = 10;

let secretNumber = Math.floor(Math.random() * (MAX - MIN + 1)) + MIN;

let guesses = 0; // for storing the number of guesses
let hint = ''; // for storing hint
let number = 0;
do {
  // get input from user
  let input = prompt(`Please enter a number between ${MIN} and ${MAX}` + hint);

  // get the integer
  number = parseInt(input);

  // increase the number of guesses
  guesses++;

  // check input number with the secret number provide hint if needed
  if (number > secretNumber) {
    hint = ', and less than ' + number;
  } else if (number < secretNumber) {
    hint = ', and greater than ' + number;
  } else if (number == secretNumber) {
    alert(`Bravo! you're correct after ${guesses} guess(es).`);
  }
} while (number != secretNumber);


for (let i = 0; i < 5; i++) {
  console.log(i);
  if (i == 2) {
    break;
  }
}

let i = 0;

while (i < 5) {
  i++;
  console.log(i);
  if (i == 3) {
    break;
  }
}

CONTINUE //////////////////////
for (let i = 1; i <= 10; i++) {
  if (i % 2 !== 0) {
    continue;
  }
  console.log(i);
}

let i = 0;
while (i < 10) {
  i++;
  if (i % 2 === 0) {
    continue;
  }
  console.log(i);
}


7-DARS  //////////////////////////////////////////////////

### switsh - taqoslash operatori

let a = +prompt("Bahoyingizni kiriting");
if(Number.isInteger(a) && a >0 && a < 6){
    switch (a){
        case 1 :
            console.log(`Sizning bahoyingiz(' ${a} ')  yomon `);
            break;
        case 2 :
            console.log(`Sizning bahoyingiz(' ${a} ')  qoniqarsiz `);
            break;
        case 3 :
            console.log(`Sizning bahoyingiz(' ${a} ')  qoniqarli `);
            break;
         case 4 :
            console.log(`Sizning bahoyingiz(' ${a} ')  yahshi `);
            break;
        case 5 :
            console.log(`Sizning bahoyingiz(' ${a} ')  alo `);
            break;   
    }
}else{
    console.log("Xato !");
}


### if else -shartli operator

let a = +prompt("a sonini kiriting");
let b = +prompt("b sonini kiriting");
if (a % 2 == 1 && b % 2 == 1){
    console.log("siz kiritga ikkala son ham tog son");
}else{
    console.log("sizkiritgan sonlar ten tog bo'lishligi kerak")
}

### Global scope

// let a = 3;

// var b = 4;

// const c = 5;

// if (true) {

//   console.log(a);

//   console.log(b);

//   console.log(c);
// }

// switch (a) {

//   case 3:

//     console.log(a);

//     console.log(b);

//     console.log(c);

//     break;
// }


### Local or Function scope

// function add() {

//   let a = 3;

//   var b = 4;

//   const c = 5;

// }

// add();

// console.log(a);

// console.log(b);

// console.log(c);


### For loop

// for (initializer; condition; iterator) {

//   // statements

// }

// for (let i = 1; i <= 10; i++) {

//   console.log(i);

// }

// for (let i = 2; i <= 10; i += 2) {

//   console.log(i);

// }

### While loop

 // while (condition) {

//   // code block to be executed

// }

// let i = 1;

// while (i <= 10) {

//   console.log(i);

//   i++;

// }

// let count = 1;

// while (count <= 10) {

//   console.log(count);

//   count += 1;

// }


8-DARS///////////////////////////////////////////////////////

### Mavzu: Funcsiya , funcsiyanig asosiy 3 ta turi :

- Function declaration

- Function expession

- Arrow function


### 1. F U N C T I O N S


Funksiya - JavaScript dasturlash tilining asoslaridan biri bo'lob uning yordamida malum bir vazifani bajarish mumkun . Funksiya boshqa bir kod qismida chaqirilganda ishga tushadi . Funksiya yordamida kodni qayta ishlatishlik imkoni mavjud yani birmarotaba elon qilib , bir necha joyda ishlatishlik imkoni mavjud , o'hshati lozim bo'lsa SCSS degi mixsend larga qisman o'hshab ketadi.

- Sintactisti quydagicha :
```

function square(number) {
 return number * number;
}



function power(a,n){
    let b = a**n;
    return b
}

console.log(power(3,2));

// natija ==> 9 


```


### Function declaration
Funktsiya deklaratsiyasi nima? Funktsiya deklaratsiyasi funktsiyani belgilaydigan identifikatorni kiritadi va ixtiyoriy ravishda funktsiya parametrlarining turlarini (prototipi) belgilaydi. Funktsiya e'lonlari (ta'riflardan farqli o'laroq) fayllar ko'lami bilan bir qatorda blok doirasida ham paydo bo'lishi mumkin.

Funktsiya declaration qolganlaridan yanabir kuchli farqi uni elon qilib olganimazdan so'ng istalgan joyda chaqirib ishlata olamiz hatto funksiya elongqilingan satirdan yuqorida chaqirib ham !

```


function sonBoluvch(n) {
    for (let i = 1 ; i < n ; i++) {
        if(n % i == 0){
            console.log(i);
        }
    }
}
sonBoluvch(10);



```

### Function expession
Function expession sintaksis jihatdan huddi declaration ohshaydi , asosiy farq bu funksiya nomi bo‘lib yani declarationda biz funcsiyaga nim bergan bo'lsak bunda o'zgaruvchi elon qilib unga funcsiyani elon qilib ketamiz va chaqirib olishda shu o'zgaruvchi nomi bilan chaqirib olamiz , yana bir asosiy farqi uni o'zidan yoqorida chaqira olmaymiz !

Function expession afzalig jihatilaridan biri shuki unu yan ihtiyori bir ozgaruvchiga tenglab , ihtiyoricha o'zlashtirib ishlatishligimiz mumkun , buni 2- misolda ko'rsak yanayam tushunarliroq bo'ladi !

```

const funcNam = function () {
    console.log("Lesson - 8");
}

funcNam(); // natija ==>  Lesson - 8

// -------------- 2 - misol -----------------

const funcNam = function (a , b) {
    console.log(a+b);
}

funcNam(4,6); // natiga ==> 10

let test = funcNam ;

test(20,67); // ===>  87 


```

### Arrow function
Arrow function hozirgacha ko'rgan funcsiyalarimiz ichida va umumiy jihatda eng ko'p ishlatladigan funcsiya bo'lib hisoblanadi u ishlash jihatidan avalgi korganlarimiz bilan birhiln ish bajaradi sintacsistida biroz far qiladi unin misolda ko'rsak yanayam tushunarliroq bo'ladi.

Arrow function yana bir avzalligi uni stentminti birdona bo'ladigan bo'lsa uni hechqanday bloc skoplarsiz yan " { } " yai figurni qavuslarsiz bir qatorning o'zida yozib ketsak ham boladi 1- misolda ko'rishligimiz mumkun


```


// ---------  1- misol  -------

const funcNam = () => console.log("hello");

funcNam(); // natija ===> hello

// -------- 2 misol--------------------------

const funcNam = (a, b , c) => {
    if(a>b && b>c){
        console.log(a+b/c);
    }else{
        console.log(a+b+c);
    }
};

funcNam(20,12,4); // natija ==> 23



```

 13- DARS ////////////////////////////////////////////////////////

 # lesson- 13 Array va String


### 1 - Array

Array - bir vaqitning o'zida bir nechta qiymatlarni o'zida saqlashi mumkun bo'lgan obect. uni ikki hil ko'rinishda yaratishlik mumkun : 1- ko'rinishii va eng ko'p qo'lanadiga usul bu ( [ ] ) figurni qavuslar ichida yozishlik , 2- uslibi esa (new) kalit so'zidan foydalanib.



M:

// 1- misol

let arrayName = ['js' ,'java' , 'go'];

// 2- misol

let arrayName = new Array('js' ,'java' , 'go');


### Array'dan element olish

Array - elementlarini uning indexslaridan foydalanib oloshligimiz mumkun . Array elementlarining raqamlari ( 0 ) - dan boshlanadi.

M:

let arrayName = ['js' ,'java' , 'go'];
console.log(arrayName[0]); // natija ==> js
console.log(arrayName[2]); // natija ==> go

### Array'ga element qo'shish

Array'ga element qo'shish uchun " push() " va " ushift() " metodlaridan foydalanishligimiz mumkun . Bunda " push() " - metodi bizga massivnig ohiridan element qo'shin=b bersa " ushift() " meto'di esa aksincha boshidan element qo'shinb beradi , yaqshiroq tushunishlik uchun misol koramiz.

M:

// push() metodiga misol

let name =  ['js' ,'java'];
name.push('go');
console.log(name); //natija =>  ['js' ,'java' , 'go']

//unshift metodiga misol

let name =  ['java' , 'go'];
name.unshift('js');
console.log(name); //natija =>  ['js' ,'java' , 'go']


## 1. String metodlari

- String length: Matn uzunligini qaytaradi.

M:

var str = "Hello";
console.log(str.length); // 5


- String charAt(): Berilgan indeksdagi belgini qaytaradi.

M:

var str = "Hello";
console.log(str.charAt(1)); // "e"

- String charCodeAt(): Berilgan indeksdagi belgining Unicode qiymatini qaytaradi.

M:

var str = "Hello";
console.log(str.charCodeAt(1)); // 101

- String [ ]: Matndagi belgi indeks orqali qaytariladi.

M:

var str = "Hello";
console.log(str[1]); // "e"

- String slice(): Berilgan indekslar orasidagi qismni kesib olish.

M:

var str = "Hello, World!";
console.log(str.slice(7, 12)); // "World"

- String substring(): Berilgan indekslar orasidagi qismni kesib olish (slice bilan bir xil, lekin manfiy indekslar bilan ishlaydi).

M:

var str = "Hello, World!";
console.log(str.substring(7, 12)); // "World"

lesson- 9 Array va String
1 - Array
Array - bir vaqitning o'zida bir nechta qiymatlarni o'zida saqlashi mumkun bo'lgan obect. uni ikki hil ko'rinishda yaratishlik mumkun : 1- ko'rinishii va eng ko'p qo'lanadiga usul bu ( [ ] ) figurni qavuslar ichida yozishlik , 2- uslibi esa (new) kalit so'zidan foydalanib.

M:

// 1- misol

let arrayName = ['js' ,'java' , 'go'];

// 2- misol

let arrayName = new Array('js' ,'java' , 'go');

Array'dan element olish
Array - elementlarini uning indexslaridan foydalanib oloshligimiz mumkun . Array elementlarining raqamlari ( 0 ) - dan boshlanadi.

M:

let arrayName = ['js' ,'java' , 'go']; console.log(arrayName[0]); // natija ==> js console.log(arrayName[2]); // natija ==> go

Array'ga element qo'shish
Array'ga element qo'shish uchun " push() " va " ushift() " metodlaridan foydalanishligimiz mumkun . Bunda " push() " - metodi bizga massivnig ohiridan element qo'shin=b bersa " ushift() " meto'di esa aksincha boshidan element qo'shinb beradi , yaqshiroq tushunishlik uchun misol koramiz.

M:

// push() metodiga misol

let name = ['js' ,'java']; name.push('go'); console.log(name); //natija => ['js' ,'java' , 'go']

//unshift metodiga misol

let name = ['java' , 'go']; name.unshift('js'); console.log(name); //natija => ['js' ,'java' , 'go']


IIFT function va Array meto'dlari
1. IIFT function
IIFT function - o'zini o'zi chaqiruvchi funcsiya ham dep atasak bo'ladi sababini esa misolda ko'rib yanayam yahshiroq tushunib olamiz
M :

(function (arg1 , arg2){
    consile.log(arg1 + arg2);
})(11 ,10); 
// natija => 21 
2. Array
Array - bir vaqitning o'zida bir nechta qiymatlarni o'zida saqlashi mumkun bo'lgan obect. uni ikki hil ko'rinishda yaratishlik mumkun : 1- ko'rinishii va eng ko'p qo'lanadiga usul bu ( [ ] ) figurni qavuslar ichida yozishlik , 2- uslibi esa (new) kalit so'zidan foydalanib.
M :

// 1- misol

let arrayName = ['js' ,'java' , 'go'];

// 2- misol

let arrayName = new Array('js' ,'java' , 'go');

Array'dan element olish
Array - elementlarini uning indexslaridan foydalanib oloshligimiz mumkun . Array elementlarining raqamlari ( 0 ) - dan boshlanadi.
M :

let arrayName = ['js' ,'java' , 'go'];
console.log(arrayName[0]); // natija ==> js
console.log(arrayName[2]); // natija ==> go
Array'ga element qo'shish
Array'ga element qo'shish uchun " push() " va " ushift() " metodlaridan foydalanishligimiz mumkun . Bunda " push() " - metodi bizga massivnig ohiridan element qo'shin=b bersa " ushift() " meto'di esa aksincha boshidan element qo'shinb beradi , yaqshiroq tushunishlik uchun misol koramiz.
M :

// push() metodiga misol

let name =  ['js' ,'java'];
name.push('go');
console.log(name); //natija =>  ['js' ,'java' , 'go']

//unshift metodiga misol

let name =  ['java' , 'go'];
name.unshift('js');
console.log(name); //natija =>  ['js' ,'java' , 'go']

Array elemeni ozgartirish
Array elemeni ozgartirishlik uschun unig index'slaridan foydalansak bo'ladi.
M :

let name =  ['js' ,'java' , 'go' ];
console.log(name); //natija =>  ['js' ,'java' , 'go']
name[1]='c++';
console.log(name); //natija =>  ['js' ,'c++' , 'go']

Array elementlarini o'chirish
Array - elementlarini o'chirishlik uchun "pop( )" va "shift( )"metodlaridan foydalansak bo'ladi , bubda "pop( )" - metodi massiv ichidagi ohirgi elamentni o'chiradi va o'chirilgan elamentni ham qaytarish imkoni mavjuv bu metodda , "shift( )"- metodi massiv ichidagi boshidagi elamentni o'chiradi va o'chirilgan elamentni ham qaytarish imkoni mavjuv bu metodda.
M :

// "pop()" metodi 

const name = ['js' , 'java' , 'go' , 'c++' , 'c#'];
const name2 = name.pop();
console.log(name); // natija => ['js' , 'java' , 'go' , 'c++' ]
console.log(name2); // natija => c#

//----------------------------------------------------------

//"shift()" metodi

const name = ['js' , 'java' , 'go' , 'c++' , 'c#'];
const name2 = name.shift();
console.log(name); // natija => [ 'java' , 'go' , 'c++' , 'c#' ]
console.log(name2); // natija => js
Array uzunligini aniqlash
Array uzunligini yani uning ichidagi conini aniqlashlik uchun ( lenght ) - hususiyatidan foydalanamiz .
M :

const name = ['js' , 'java' , 'go' , 'c++' , 'c#'];
console.log(name.lenght); // natiga ==> 5
concat() Metod
concat() -metodi ikki yoki undan ortiq arraylarni bitlashtiridshlik uchun ishlatiladi . bu ularni birlashtiradi va natiga qaytaradi .
M :

const array1 = [ 1, 4 ];
const array2 = [ 2, 3, 7 , 9 ];
const result = array1.concat(array2);
console.log(result); // natija ==> [1, 4, 2, 3, 7, 9]
indexOf() va lastIndexOf() Metodlari:
indexOf() belgilangan elementni birinchi marta qaysi indeksda ekanligini qaytaradi, lastIndexOf() esa oxirgi marta qaysi indeksda ekanligini.
M :

let fruits = ["apple", "banana", "kiwi", "melon", "banana"];
console.log(fruits.indexOf("banana")); // 1
console.log(fruits.lastIndexOf("banana")); // 4
find() metodi
find() - metodi birinchi bo;lib shart bajargan array elamentini qaytaradi , kopincha bu metod array ichida meto'd qaytarishlikda ishlatiladi.
M :

const result = [1, 4, 2, 3, 7, 9 ];
const findValue = (n) => n === 2 ;
const findValue2= result.find(findValue);
console.log(findValue2); // natiga  => 2 
// agar shartga tushmasa undefaind qaytaradi misol uchun n === 5 korinishini kiritsak.
splice(start, deleteCount, item1, ..., itemN) Metodi:
splice() metodi massivda belgilangan indeksdan boshlab ma'lum bir soni o'chiradi va/ya yangi element(lar)ni qo'shadi.
M :

let fruits = ["apple", "banana", "orange", "grape"];
fruits.splice(2, 1, "kiwi", "melon");
console.log(fruits); // natija ==>  ["apple", "banana", "kiwi", "melon", "grape"]

slice(start, end) Metodi:
slice() metodi massivning belgilangan oraliqni ko'chirib olish uchun ishlatiladi.
M :

let fruits = ["apple", "banana", "kiwi", "melon", "grape"];
let subArray = fruits.slice(1, 4);
console.log(subArray); //natija ==> ["banana", "kiwi", "melon"]

indexOf() va lastIndexOf() Metodlari:
indexOf() belgilangan elementni birinchi marta qaysi indeksda ekanligini qaytaradi, lastIndexOf() esa oxirgi marta qaysi indeksda ekanligini.
M :

let fruits = ["apple", "banana", "kiwi", "melon", "banana"];
console.log(fruits.indexOf("banana")); //natiga =>  1
console.log(fruits.lastIndexOf("banana")); //natiga =>  4

includes() Metodi:
includes() metodi massivda berilgan elementni qidiradi va mavjud bo'lsa true, aks holda false qaytaradi.
M :

let fruits = ["apple", "banana", "kiwi", "melon"];
console.log(fruits.includes("kiwi")); // true
console.log(fruits.includes("grape")); // false
filter(callback) Metodi:
filter() metodi berilgan shartlarni qondirib, shartlarni bajaradigan elementlarni qaytaradi.
M :

let numbers = [10, 25, 5, 40];
let filteredNumbers = numbers.filter(number => number > 20);
console.log(filteredNumbers); //  natija =>### map(callback) Metodi:  [25, 40]

map(callback) Metodi:
map() metodi massivning har bir elementi uchun berilgan funksiyani bajarib, yangi bir massivni qaytaradi.
M :

let numbers = [1, 2, 3, 4];
let squaredNumbers = numbers.map(number => number ** 2);
console.log(squaredNumbers); //natija =>  [1, 4, 9, 16]

/////////////////////////////////////////////////////////////////////


## DOM - Document Object Model

### DOM - Selectors 
1. getElementById('')
2. getElementByTegName('')
3. getElementByClassName('')
4. getElementByName('')
5. qutSelector('')
6. qutSelectorAll('')

- getElementById('')-> bunda biz elamentimizni  " id " nomiorqali tanlab olamiz . 
<p>M :</p>

let catd = .document.getElementById('card')

- getElementByClassName('')-> bunda biz elamentimizni " class " nomi orqali tanlab olamiz . 
<p>M :</p>

let catd = .document.getElementByClassName('card');
- getElementByTagName('')-> bunda biz elamentimizni " teg " nomi orqali tanlab olamiz . 
<p>M :</p>

let h1 = .document.getElementByTagName('h1');

- getElementByName('')-> bunda biz elamentimizni " name " nomi orqali tanlab olamiz . 
<p>M :</p>

let catd = .document.getElementName('card');
- qutSelector('')-> bunda biz elamentimizni ham " .class , #id , tegName , name " orqali tanlab olishligimiz mumkun  . 
<p>M :</p>

let card = document.querySelector(".card");
//----------------------
let card = document.querySelector("#card");
//-----------------------
let card = document.querySelector("h1");
//-------------------------
let card = document.querySelector("card");

- qutSelectorAll('')-> bunda biz elamentimizni ham " .class ,  tegName , name " orqali qancha bo'lsa hammasini tanlab  olishligimiz mumkun  . 
<p>M :</p>

let card = document.querySelectorALL(".card");
//----------------------
let card = document.querySelectorAll("h1");
//-------------------------
let card = document.querySelectorAll("card");

<hr>

### Tanlab olgan elamentlarimiz ustida bajarishimiz mukun bo'lgan ammallar

- element.parentElement -> bu bizga tanlab olgan elamentimizni parent 'ota' elamentini ko'rsatadi.

- element.parentElemen.parentElement.parentElement -> bu bizga tanlab olgan elamentimizni eng katta parent elamentigacha chiqishlik imkonini beradi bu ketma ketlikda yozsak.

- element.parentNode -> bu ham bizga *.parentElement* kabi vazifa bajaradi

- element.nextElementSibling -> bu bizga tanlab olgan elamentimizdan kegingi elamentni ko'rsatadi.

- element.previosElementSibling -> bu bizga tanlab olgan elamentimizdan oldingi elamentni ko'rsatadi.

- element.chidren -> bu bizga tanlab olgan elamentimizni icidagin 'bola' elamentini ko'rsatadi.

- element.firstElementChild -> bu bizga tanlab olgan elamentimizni ichidagi birinchi  elamentni ko'rsatadi.

- element.lastElementChild -> bu bizga tanlab olgan elamentimizni ichidagi ohirgi  elamentni ko'rsatadi.

- element.style -> bu bizga tanlab olgan elamentimiz olishi mumkun bo'lga barcha srillarni ( *Object { }*) ro'yhat korinishida ko'rishligimiz mumkun va shu orqali elamentimizni manipulatsiya yani stillarni o'zgartiishimiz yoki qo'shimcha yana stillar qo'shishligimiz mumkun.
<p>M : </p>

let element = document.querySelector("h1");
element.style.color = "red";


### Dynamicolly DOM monupulating
- createElement(tegName);
- appennd();
- prepend();
- after();
- before();
- createElement(tegName) -> bizga yangi html elament qurib beradi .
- let div = document.createElement(div);

// natija -> <div></div>
1. appennd() -> yaratgan elamentimizni tanlab olgan elamentimiz ichiga joylashtirib beradi , joylashtirishda elamentimizni ohiridan joylashtiradi.
let wrapper =document.querySelector('.wrapper');
let card = document.createElement('div');

2. wrapper.append(card);
prepend() -> yaratgan elamentimizni tanlab olgan elamentimiz ichiga joylashtirib beradi , huddi 'appennd()' singari farqi bunda joylashtirishda elamentimiz boshidan joylashtiradi, ikkisini bir vaqitda ishlatilmaydi .
let wrapper =document.querySelector('.wrapper');
let card = document.createElement('div');

3. wrapper.prepend(card);
after() -> yaratgan elamentimizni tanlab olgan elamentimizni pasidan qo'shib beradi.
 let wrapper=document.querySelector('.wrapper');
 let card = document.createElement('div');

 wrapper.after(card);
4. before() -> yaratgan elamentimizni tanlab olgan elamentimizni yuqorisidan qo'shib beradi.

```
let wrapper =document.querySelector('.wrapper');
let card = document.createElement('div');

wrapper.before(card);
```