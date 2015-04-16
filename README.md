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
