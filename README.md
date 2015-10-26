#Scroll-To-Top jQuery plugin

Версия: **1.0.0**

###Для чего плагин?
* Плагин для автоматической прокрутки в верх страницы при нажатии на кнопку "Top^";
* Отображение кнопки автоматически при прокрутке страницы вниз на заданную высоту;
* Работает как на десктопной, так и на мобильной версии сайтов.

##Зависимости
* **JQuery** - необходимая библиотека для работы модуля

##Установка с помощью Bower
`bower install jquery-scrolltotop --save` - происходит установка плагина. В текущем пакете есть зависимость jquery. Если jquery не были установлены через bower, он установится вместе с плагином ScrollToTop. 


###Как подключить плагин

Подключите файлы в HTML проект:
```html
// Scrolltotop плагин
<script src="url-to-module/jquery-scrolltotop/jquery.scrolltotop.js"></script>
// Стили
<link rel="stylesheet" href="url-to-module/jquery-scrolltotop/jquery.scrolltotop.css">

// JQuery
<script src="http://code.jquery.com/jquery-2.1.4.min.js"></script>

```


##Описание параметров
```js
$.scrolltotop ({аргументы функции}); 
```
Тип входящих данных: JSON
Варианты входящих данных:

* **top_standoff** - Минимальная высота в пикселях от верха страницы, при которой отображается кнопка прокрутки страницы. Значение по умолчанию - `700`;
* **speed** - Скорость прокрутки в мс до верха страницы. Значение по умолчанию - `400`;
* **segment** - Значение по умолчанию - `TRUE`;
	* Если параметр **segment** будет равен `TRUE`, то скорость прокрутки высчитывается из формулы **(высота всей прокрутки экрана / значение top_standoff) * speed**. Т.е. будет происходить плавная прокрутка всей страницы, вне зависимости от длинны прокрутки страницы с заданной скоростью **speed** для каждого интервала **top_standoff** на странице.
	* Если параметр **segment** будет равен `FALSE`, то скорость прокрутки всей страницы будет равно скорости, заданной параметром **speed**, вне зависимости от высоты страницы;
* **class** - Задаем имя класса для кнопки прокрутки. По умолчанию значение `scroll1`.
* **object_id** - Задаем ID кнопке прокрутки. По умолчанию значение `jquery-scrolltotop`.


##Примеры использования
Для активации плагина достаточно запустить функцию
```js
$.scrolltotop (); // Плагин запустится с параметрами по умолчанию
```

Запускаем плагин со своими настройками
```js
$.scrolltotop ({top_standoff: 500, speed: 100, class: 'my_scroll_class'});
```
В этом случае запускаем плагин с измененными параметрами высоты и скорости прокрутки. А так же задаем для кнопки имя собственного класса.