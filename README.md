LLFonts - плагин для отложенный загрузки шрифтов
=====================
Подключение плагина:
```javascript
<script src="LLFonts.js"></script>
```
Инициализация плагина (производится до подключения)

Для загрузки с Google Fonts
```javascript
LLFontsConfig = {
   vlenght: 500,
   host: false,
   scrollTimeout: false,
};
```
Для загрузки со своего сайта
```javascript
LLFontsConfig = {
   vlenght: 500,
   host: true,
   scrollTimeout: false,
   files: [
        {
            font: 'Droid Sans',
            url: 'fonts/DroidSans.css'
        },
       {
           font: 'ProximaNova',
           url: 'fonts/ProximaNova.css'
       }
    ]
};
```
На странице добавляем в блок следующий код. Когда пользователь доскролливает до блока - {vlenght}px начинается загрузка шрифта
```html
<div data-font="nameFont" class="llfonts">
```
vlenght - высота перед блоком когда начнется загрузка шрифта
host - в случаи true загружается с хоста, для работы требуется {files} где указаны названия и пути к файлом css. В случаи false загружает с Google Fonts 
scrollTimeout - реализует debounce (пока пользователь не перестанет скролить загрузка не начнется). 

