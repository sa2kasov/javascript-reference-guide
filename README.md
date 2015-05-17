<p align="center">
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/archive/6/6a/20120221235432%21JavaScript-logo.png"
      height="400" width="400" alt="JavaScript Logo"
    />
</p>

# JavaScript: Справочное руководство

### Содержание

1. [История появления](#История-появления)
	1. [Создатель языка о его происхождении](#Создатель-языка-о-его-происхождении)
2. [Введение в JavaScript](#Введение-в-JavaScript)
3. [Комментарии](#Комментарии)
4. [JavaScript в HTML](#JavaScript-в-HTML)
5. [Переменные](#Переменные)
6. [Операторы](#Операторы)
	1. [Арифметические](#Арифметические-операторы)
	2. [Операторы сравнения](#Операторы-сравнения)
	3. [Логические операторы](#Логические-операторы)
7. [Выражения и инструкции](#Выражения-и-инструкции)
8. [Типы данных](#Типы-данных)
	1. [Логический тип](#Логический-тип)
	2. [Числа](#Числа)
	3. [Строки](#Строки)
		1. [Экранирование символов](#Экранирование-символов)
		2. [Конкатенация](#Конкатенация)
		3. [Сравнение строк](#Сравнение-строк)
	4. [Манипуляции с типами](#Манипуляции-с-типами)
	5. [Приведение типов](#Приведение-типов)
9. [Управляющие конструкции](#Управляющие-конструкции)
	1. [if](#if)
	2. [Тернарный оператор](#Тернарный-оператор)
	3. [switch](#switch)
	4. [for](#for)
	5. [while](#while)
	6. [do..while](#dowhile)
	7. [for..in](#forin)
	8. [Метки](#Метки)
	9. [try..catch..finally](#trycatchfinally)


## История появления

Основатель языка, Брендан Айк (англ. Brendan Eich) – программист и создатель языка программирования JavaScript. На момент 2023 года исполнительный директор _Brave Software_. Был нанят в компанию _Netscape_ 4 апреля 1995 года, где была поставлена задача внедрить язык программирования _Scheme_ или что-то похожее в браузер Netscape. Поскольку требования были размыты Айка перевели в группу ответственную за серверные продукты, где он проработал месяц занимаясь улучшением протокола HTTP. В мае разработчик был переброшен обратно, в команду, занимающуюся клиентской частью (браузером), где он немедленно начал разрабатывать концепцию нового языка программирования.

Первоначально язык назывался _LiveScript_ и предназначался как для программирования на стороне клиента, так и для программирования на стороне сервера.

_JavaScript_ изначально был придуман для браузера _Netscape Navigator_. Microsoft первый кто позаимствовал этот язык для своего браузера _Internet Explorer_, добавив в него свои новые возможности. На что Netscape подала в суд в результате чего компания Microsoft выпустила аналог языка _JavaScript_, названный под именем _JScript_. Первым браузером, поддерживающим эту реализацию, был _Internet Explorer 3.0_.

По инициативе компании Netscape была проведена стандартизация языка ассоциацией ECMA. Стандартизированная версия имеет название _ECMAScript_. Первой версии спецификации соответствовал _JavaScript_ версии 1.1. _JavaScript_ после своего появления отличался оригинальностью и настолько понравился, что его начали портировать не только в браузеры, но и в другие среды.

### Создатель языка о его происхождении

Создатель языка JavaScript Brendan Eich [поделился](https://www.jwz.org/blog/2010/10/every-day-i-learn-something-new-and-stupid/) историей происхождения языка и объяснил почему он такой, какой есть:

> JS был обязан «выглядеть как Java», только поменьше, быть эдаким младшим братом-тупицей для Java. Кроме того, он должен был быть написан за 10 дней, а иначе мы бы имели что-то похуже JS.

> что-то вроде PHP, только еще хуже. Его босс Netcsape быстро «зарубил» (в июле 1995, если мне не изменяет память; я сдлелал JS в начале/середине мая), т.к. это был уже третий язык после Java и JS. Было и так трудно обосновать то, что у нас 2 новых языка программирования для web.

> В то время мы должны были двигаться очень быстро, т.к. знали, что Microsoft идет за нами.

> Считайте, что JavaScript (пожалуйста, только не «JScript») спас вас от VBScript.

> 10 дней на то, чтобы сделать лексер, парсер, компилятор в байткод (bytecode emitter), интерпретатор, встроенные классы и декомпилятор. Помощь была только с файлом jsdate.c — от Ken Smith из Netscape (который, по нашему излишне оптимистичному соглашению, склонировал java.util.Date — Y2K баги и т.д. Джеймс Гослинг...).

> Простите, времени было мало для того, чтобы сделать правильную оптимизацию хвостовой рекурсии. 10 дней почти без сна, чтобы сделать JS с чистого листа, заставить его «выглядеть как Java» (я сделал, чтобы он выглядел как C), и тайком протащить туда его спасительные фишки: first class functions (замыкания сделал позже, но они были частью плана сразу) и прототипы (примерно как в языке Self).

> I'll do better in the next life.

## Введение в JavaScript

_JavaScript_ – алгоритмический язык программирования, интерпретируемый язык сценариев, основан на синтаксисе _C_ и _Java_.

_JavaScript_ является объектно-ориентированным языком, но используемое в языке прототипирование обуславливает отличия в работе с объектами по сравнению с традиционными класс-ориентированными языками. Кроме того, _JavaScript_ имеет ряд свойств, присущих функциональным языкам: функции как объекты первого класса, объекты как списки, каррирование, анонимные функции, замыкания, ..., что придаёт языку дополнительную гибкость.

**Популярность языка**

_JavaScript_ является самым популярным языком программирования, используемый для frontend-разработки на стороне клиента. Согласно [рейтингу TIOBE Index](https://www.tiobe.com/tiobe-index), базирующемуся на данных поисковых систем Google, Bing, Yahoo!, Wikipedia, Amazon, YouTube и Baidu, на начало 2023 года JavaScript находится на :trophy: 7 месте, постоянно улучшая свои позиции за последние несколько лет. :trophy: 1 место в [рейтинге GitHub](https://octoverse.github.com/#top-languages-over-the-years) 2021 года. :trophy: 7 место в [рейтинге IEEE](https://spectrum.ieee.org/top-programming-languages-2022) (Институт инженеров электротехники и электроники) в 2022 году. По опросам разработчиков на [StackOverflow](https://survey.stackoverflow.co/2022/#section-most-popular-technologies-programming-scripting-and-markup-languages) в 2022 году JavaScript занимает :trophy: 1 место уже 10 лет подряд как самый часто используемый язык программирования.

**Некоторые отличительные особенности JavaScript:**

- Регистрозависимые конструкции, функции и операторы;
- Все идентификаторы чувствительны к регистру;
- В названиях переменных можно использовать буквы, символ подчёркивания, символ доллара, арабские цифры;
- Названия переменных не могут начинаться с цифры.

**Нотация – устоявшиеся правила записи**

* Все имена маленькими буквами;
* На стыке слов большая буква (camelStyleNotation);
* Переменные и свойства — существительные;
* Массивы и коллекции — существительные во множественном числе;
* Функции и методы — глаголы;
* Названия классов с Большой буквы.

## Комментарии

Комментарии в JavaScript могут быть строчными – начинаются с `//` и блочными (многострочными) – начинаются с `/*` и заканчиваются с `*/`.

```js
// Однострочный комментарий

/*
Многострочный
комментарий
*/
```

## JavaScript в HTML

JavaScript может быть встроен в код HTML с помощью тега `<script>`. Если подключается внешний файл скриптов, то используется атрибут `src`  в котором указывается ссылка на файл скрипта.

```html
<script src="outer.js"></script>
```

Встроенный JavaScript-код заключается между тегами `<script></script>`. Встроенный JavaScript-код будет игнорироваться если у тега указан атрибут `src`.

```html
<script>
// Код на JavaScript
</script>
```

## Переменные

- Переменная – именованный участок памяти;
- Переменные объявляются ключевым словом `let`, `const` и `var`;
- Переменные принимают тот тип данных, который в них присваивается;
- В JavaScript допускается присваивать значение переменной, которая еще не определена, но считается хорошим тоном сначала объявить переменную одним из ключевых слов (пункт 2);
- JavaScript язык с динамической типизацией и переменные являются универсальными для всех типов данных, т.е. способны хранить значения любого типа.

**Объявление и инициализация переменных**

```js
// Объявление переменных
const a
let b, c, d

// Иницилизация переменных
const a = 15
let b = c = d = 50
var e = 'string', f = false, g

// Сокращенная запись
x += 1 // Сокращенная запись x = x + 1
// Доступна и для операторов "+", "-", "*", "/", "%"
i++ // инкремент
i-- // декремент
++i // преинкремент
--i // постдекремент

// Пример
var i = 1
let a = i++ // -> a = 1; i = 2;
let b = ++i // -> b = 3; i = 3;
```

## Операторы

### Арифметические операторы

- `+` – плюс
- `-` – минус
- `*` – умножить
- `/` – разделить
- `%` – целочисленный остаток от деления

### Операторы сравнения

- `==` – сравнение
- `===` – сравнение с учетом типа
- `!=` – не равно
- `!==` – не равно с учетом типа
- `>` – больше
- `<` – меньше
- `>=` – больше или равно
- `<=` – меньше или равно

### Логические операторы

_(в порядке приоритета)_
- `!` НЕ (отрицание)
- `&&` И (конъюнкция)
- `||` ИЛИ (дизъюнкция)

```js
1 && 2 // -> 2, значение на котором скрипт остановился
1 && 0 // -> 0
0 && 1 // -> 0, т.к. первый операнд false и нет смысла идти дальше
0 || 'false' // -> "false"
```

Операторы сравнения возвращают булево значение либо `true` либо `false`.

Параметры операторов называются _операндами_. Операторы у которых два операнда называются _бинарными_, один операнд — _унарными_, три — _тернарными_ (только один унарный оператором `!` (логическое "не"));

## Выражения и инструкции

### Выражения

_Expression_

```js
5 + 10
'John'
!false
```

### Инструкции

_Statement_

```js
5 + 10
'John'
!false
```

## Типы данных

_Тип данных_ – набор операций, которые можно выполнить над данными. В JavaScript есть формально 8 типов:

1. Boolean – логический;
2. Number – числовой;
3. BigInt – числа произвольной длины;
4. String – строковый;
5. Array – массив;
6. Object – объект;

Тривиальные типы:

7. undefined – неопределенный тип, любая необъявленная переменная имеет такой тип, а также объявленные переменные, которым еще не присвоено значение или несуществующие свойства объекта;
8. null – отсутствие значения. Если переменная имеет значение _null_, то это означает, что в ней ничего не хранится.

### Логический тип

Может принимать константу `true` или `false`. При проверке значения операндов преобразуются в логический тип.

**Создание**

```js
const b = new Boolean(value) // где value значение для булева типа
```

В JavaScript есть как _Boolean-объекты_, так и примитивные _Boolean_ значения. Не смешивайте их. Объект – это объект. В частности, JavaScript любой объект считается `true`, например при неявном приведении типа в операторе `if`.

```js
const x = new Boolean(false)

if(x) {
 // этот код будет выполнен
}
```

Не используйте объект _Boolean_ для преобразования к булеву значению. Вместо этого, используйте _Boolean_ как функцию.

```js
const x = Boolean(expression) // предпочтительно
const y = new Boolean(expression) // не используйте

// с использованием двойного отрицания:
const z = !!expression 
```

На основании «правила лжи» происходит приведение к логическому типу:

* само значение `false`
* `0` или `-0` (число ноль)
* `''` (пустая строка)

Тривиальные типы

* Значение `NULL`
* `undefined`
* `NaN` (Not a Number)

В современном JavaScript-программировании `new Boolean` не используется.

### Числа

**Создание**

```js
// Полня форма
var n = new Number(value) //где value — числовое значение
//Литеральная форма записи
var n = 25
//Приведение к Number
var n = '123'
Number(n) //123
var n = '132A'
Number(n) //NaN
```

В числовой тип входят как целые числа, так и дробные. Экспоненциальные: $5E3$ (пять на 10 в третьей степени).

В JavaScript можно записать числа в 16-ричной или 8-ричной системе счисления, но только с целыми числами. Например, `const y = 0xFF;`. Префиксом числа восьмеричной системой счисления является цифра `0`. Пример: `const z = 040;` будет 32 (в 10-тичной).

**Особые числовые значения**

В тип `Number` входят не только числа, но и еще три значения:

- +бесконечность (`Infinity`);
- -бесконечность (`-Infinity`);
- особое значение `NaN` (Not a Number – значение числового типа не число). Возникает когда вычисление просто не может быть. Например:

```js
const x = 0 / 0 // -> NaN, деление на ноль
const y = Math.sqrt(-1) // -> NaN, отрицательная степень

// Является ли значение числового типа не числом?
isNaN('x' * 10) // -> true

// Является ли значение бесконечным?
isFinite() // false, если значение NaN или ±Infinity, иначе true
```

### Строки

_Строка_ – набор символов, обрамляется в апострофы или двойные кавычки.

#### Экранирование символов

_Экранирование символов_ – вставка специальных символов через знак обратного слэша после которого идет определенный символ.

* `\'` – одинарные кавычки (апостроф);
* `\"` – двойные кавычки;
* `\\` – обратный слэш (`\u005C`);
* `\b` – backspace;
* `\f` – form feed;
* `\n` – переход на новую строку (`\u000A`);
* `\r` – возврат каретки (`\u000D`);
* `\t` – табуляция (`\u0009`);
* `\v` – вертикальная табуляция;
* `\0` – символ NULL (`\u0000`);
* `\ddd` – octal sequence (3 digits: ddd);
* `\xdd` – hexadecimal sequence (2 digits: dd). Символ Latin-1, заданный двумя шестнадцатеричными цифрами;
* `\udddd` – unicode sequence (4 hex digits: dddd). Символ Unicode, заданный четырьмя шестнадцатеричными цифрами.

В JavaScript все хранится в кодировке _Unicode_. Это означает, что мы можем использовать любые символы _Unicode_ прямо в строке (в Юникоде первые 128 символов совпадают с соответствующими символами в ASCII).

```js
// Полное обозначение символа Unicode
const s1 = '\u2014' // Длинное тире (—)
'\u2564' // Денежный знак валюты тенге (₸)

// Шестнадцатеричное
const s2 = '\x20' // Пробел
```

#### Конкатенация

_Конкатенация_ – объединение (сцепление) строк.

```js
"I " + 'am ' + `in ` + "love " + 'with ' +  ` JavaScript`
```

#### Сравнение строк

Строки сравниваются в соответствии со своей позицией в Unicode.

```js
'a' > 'A' // -> true
```

### Манипуляции с типами

```js
'2' + '2' // -> строка "22"
2 + '2' // -> строка "22" (строка приоритетнее числа)
'' + true // -> строка "true" (строка приоритетнее булев типа)
2 + true // -> число 3 (число приоритетнее булев типа)
'2' * 10 // -> число 20 (если строка может быть преобразована в число)
'x' * 10 // -> NaN (Not a Namber)

const x = 'x' * 10 // -> NaN
const y = 'y' * 10 //-> NaN
// Однако
x == y // -> false, т.к. NaN != NaN
```

Для проверки типа есть оператор определения типа typeof возвращающая строку соответствующего типа.

```js
typeof 5 // "number"
typeof true // "boolean"
typeof '5' // "string"
```

### Приведение типов

В JavaScript основными преобразованиями типов являются строковые, числовые и логические.

**Преобразование в число**

Числовое значение дают следующие преобразования:

* Умножение строки (которая состоит только из чисел) на число;
* Передать значение как аргумент функции `Number`;
* `parseInt()` – целое число из значения до тех пор, пока не встретится нечисловое значение;
* `parseFloat()` – дробное число из нечислового значения, тоже что и `parseInt()`, но допускается вхождение символа точки.

```js
'5' * 1 // -> целое число 5
'5.5' * 1 // -> дробное число 5.5

parseInt('100.1JS') + 1 // -> целое число 101
parseFloat('10.5JS') // -> дробное число 10.5

Number(true) // -> число 1
Number(false) // -> число 0
```

**Преобразование в строку**

* Строковое преобразование имеет приоритет при попытке сложения двух значений;
* Передача значения как аргумент функции `String`;
* Если в объекте реализован метод `toString()` он будет использован при попытке преобразования объекта в строку.

```js
5 + '' // -> строка '5'
String(true) // -> строка "true"
false + '' // -> строка "false"
```

**Логическое преобразование**

* Логическое сравнение преобразуется для значений при попытке их логического сравнения (`==`, `===`, `&&`, `||` и `!`), в условных конструкциях `if`, `while`, `switch`;
* В логическое значение преобразует функция `Boolean()`.

```js
!!5; // -> true
Boolean(15); // -> true
```

## Управляющие конструкции

### if

Управляющая конструкция `if` выполняет инструкции если условие истинно.

В `if` может быть сколько угодно `else if`. Последнее `else` (без условий) можно опустить, хотя рекомендуется его использовать как «отстойник».

```js
if (condition) {
   statement1
   statement2
} else if (condition 2) {
   statement3
   statement4
} else {
   statement5
   statement6
}
```

### Тернарный оператор

_Тернарный оператор_ – это оператор с тремя операндами. В JavaScript единственный тернарный оператор это сокращенный вариант записи условной конструкции `if..else..`.

```js
const result

// Обычная условная конструкция
if (условие)
  result = 'условие истинно'
else
  result = 'условие ложно'

// То же условие через тернарный оператор
b = (a > 1) ? 'условие истинно' : 'условие ложно'
```

Скобки в условии тернарного оператора можно опустить, но для лучшей читаемости не рекомендуется.

### switch

Оператор переключения `switch` позволяет проанализировать множество вариантов значений, используя для анализа числовое или строковое значение.

Внутри конструкции `switch` обычно применяют оператор `break`, т.к. в отсутствии данного оператора если `switch` встретит значение которое соответствует значению в `case`, он выполнить все последующие (нижележащие) инструкции игнорируя все `case` словно их нет.

Оператор `default` сработает если интерпретатор не попадет ни в один `case`.

```js
const a = 2

switch (a) {
  case 0:
  case 1:
  case 2:
    console.log('Two')
    break;
  case 3:
  case 4:
  case 5:
  default:
    alert("It's many!")
}
```

### for

Цикл `for` – многократное выполнение одних и тех же действий заранее известное количество раз.

_Итерация_ – однократное выполнение (шаг) цикла.

**Как работает цикл for**

```js
for (часть A; часть B; часть C)
  часть D (тело цикла)
```

Когда интерпретатор встречает цикл `for`, он сперва заходит в `часть А` и выполняет то, что там написано ровно один раз. `часть В` выступает как условие, если оно истинно, то интерпретатор заходит в `часть D` (тело цикла), после выполнения которого переходит в `часть С`. Потом возвращается в `часть В` (проверяет условие) и если там истина, то переходит в `часть D` и далее как по треугольнику происходит переход:

> часть В => часть D (тело цикла) => часть С
>
> До тех пор пока часть В не вернет false

Любую из частей цикла for можно опустить, главное чтобы присутствовали точки с запятой как часть синтаксиса.

Если в `часть А` необходимо выполнить несколько инструкций, то разделять их следует запятой.

**Цикл for с пустым телом**

Ниже цикл возводит значение переменной `result` в 10-ую степень.

```js
for (let i = 1, result = 2, exp = 10; i < exp; result += result, i++){}
console.log(result) // -> 1024
```

**Цикл for с continue и break**

`continue` в циклах `for`, `while` и `do..while` прерывает текущую итерацию и переход к следующей.

`break` немедленно заканчивает цикл и выходит за операторные скобки.

```js
for (let i = 0; i < 10; i++) {
 if (i == 4)
   continue

 if (i == 8)
   break
}
```

### while

* Условие проверяется ПЕРЕД очередным проходом;
* Выполняется пока условие истинно;
* Если условие изначально ложно – не выполнится ни разу.

```js
let num = 1

while (num < 1000) {
 num *= 2
 if(num == 32) continue
 if(num == 512) break
 console.log(num)
}
```

### do..while

* Условие проверяется ПОСЛЕ очередного прохода;
* Выполняется пока условие истинно;
* Если условие изначально ложно – выполнится хотя бы один раз.

```js
let num = 1

do {
   num *= 2
   if (num == 32) continue
   else if (num == 512) break
   console.log(num)
} while (num < 1000)
```

Если в теле цикла `do..while` все лишь одна инструкция, то операторные скобки можно опустить.

```js
let a = 0
do a++
while (a <= 5) // Одна инструкция в теле цикла
console.log(a) // -> 5
```

### for..in

Предназначен для прохода по массивам, коллекциям, объектам.

```js
for (let prop in navigator) {
  console.log(prop)
}
```

### Метки

Иногда бывает нужно прервать вложенный цикл или цикл с n-количеством вложенности. В JavaScript это можно организовать с помощью меток. Названия меток не должны начинаться с цифры.

```js
let i = 1

outer: while (i < 10) {
 inner: for (var j = 1; j <= i; j++) {
   if (j > 2)
    continue inner
   if (i * j > 10) {
     console.log(i, j)
     break outer
   }
 }
 i++
} // -> 6, 2
```

### try..catch..finally

`try..catch..finally` – оператор обработки исключений служит для написания кроссбраузерных приложений. Так как при возникновении ошибки в JavaScript исполнение программы останавливается, конструкция `try..catch..finally` позволяет пропустить ошибочную конструкцию и перейти к следующей.

Сначала JavaScript пытается выполнить все что находится в блоке `try`, если внутри блока `try` ошибки не возникнет, то содержимое блока `catch` игнорируется.

Содержимое блока `finally` выполняется при любом случае, вне зависимости от того возникла ошибка или нет.

Разница между кодом в блоке `finally` и кодом в блоке всей этой конструкции проявляется в JavaScript только в случае если в блоке `catch` произойдет ошибка.

В случае возникновения ошибки в `catch` программа остановится за исключением если есть блок `finally`. В таком случае блок `finally` выполнится, а все что после него нет.

Допускается вкладывать конструкции `try..catch..finally` внутри друг друга.

```js
try {
  console.log('До ошибки в блоке try')
  throw new Error() // В случае ошибки попадаем в блок catch
   console.log('После ошибки в блоке try')
} catch(e) { // В переменную "e" заносится информация об ошибке
  console.log('Сообщение об ошибке: ' + e.message)
} finally {
  console.log('Сообщение из блока «finally»')
}

console.log('Сообщение после конструкции try..catch..finally')
```
