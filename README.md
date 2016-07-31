[![GitHub version](https://badge.fury.io/gh/fater%2Fjquery-scrolltotop.svg)](https://badge.fury.io/gh/fater%2Fjquery-scrolltotop)

jQuery Scroll-To-Top Plugin

Plugin version: **1.0.2**

###What does the plugin?
* Отображение кнопки автоматически при прокрутке страницы вниз на заданную высоту;
* Плагин для автоматической прокрутки в верх страницы при нажатии на кнопку "Top^";
* Работает как на десктопной, так и на мобильной версии сайтов.

![jQuery Scroll To Top Plugin](http://files.fater.ru/git/jquery-scrolltotop/1.gif)

##Зависимости
* **jQuery** - необходимая библиотека для работы модуля

##Установка с помощью Bower
```
$> bower install jquery-scrolltotop --save
```
Происходит установка плагина. В текущем пакете есть зависимость [jQuery](http://jquery.com/). Если [jQuery](http://jquery.com/) не были установлены через [Bower](http://bower.io/), он установится вместе с плагином ScrollToTop. 


###Как подключить плагин

Подключите файлы в HTML проект:
```html
// Scrolltotop плагин
<script src="url-to-module/jquery-scrolltotop/dist/jquery.scrolltotop.min.js"></script>
// Стили
<link rel="stylesheet" href="url-to-module/jquery-scrolltotop/dist/jquery.scrolltotop.min.css">

// JQuery
<script src="http://code.jquery.com/jquery-2.1.4.min.js"></script>

```

##Описание параметров
```js
$.scrolltotop({аргументы функции}); 
```
Тип входящих данных: JSON
Варианты входящих данных:

Параметр | Описание | Значение по умолчанию
--- | --- | ---
**top_standoff** | Минимальная высота в пикселях от верха страницы, при которой отображается кнопка прокрутки страницы. | *700*
**speed** | Скорость прокрутки в мс до верха страницы. | *400*
**segment** | <ul><li>Если параметр **segment** будет равен `TRUE`, то скорость прокрутки высчитывается из формулы **(высота всей прокрутки экрана / значение top_standoff) * speed**. Т.е. будет происходить плавная прокрутка всей страницы, вне зависимости от длинны прокрутки страницы с заданной скоростью **speed** для каждого интервала **top_standoff** на странице.</li>	<li>Если параметр **segment** будет равен `FALSE`, то скорость прокрутки всей страницы будет равна скорости, заданной параметром **speed**, вне зависимости от высоты страницы</li></ul> | *True*
**class** | Задаем имя класса для кнопки прокрутки. | *scroll1* 
**object_id** | Задаем ID кнопке прокрутки.| *jquery-scrolltotop* 


##Примеры использования
Для активации плагина достаточно запустить функцию
```js
$.scrolltotop(); // Плагин запустится с параметрами по умолчанию
```

Запускаем плагин со своими настройками
```js
$.scrolltotop({top_standoff: 500, speed: 100, class: 'my_scroll_class'});
```
В этом случае запускаем плагин с измененными параметрами высоты и скорости прокрутки. А так же задаем для кнопки имя собственного класса.