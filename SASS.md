Переменные   
`$var_name: value ;` - инициализация переменной

---

Element state   
`&:hover { code }` - define state of element

---
 
 Классы   
`.parent_class { code }` - класс родитель   
`.child_class { @extend .parent_class; code }` - наследование от класса родителя

---

Импорты   
`@import 'scss_file_name';` - импорт файла   
Все названия файлов должны совпадать с патерном  `_fileName.scss`

---

Миксины   
`@mixin function_name ($params) {}` - создание функции   
`.class_name {@include function_name (params);}` - вызов функции   

пример:

@mixin border-radius($radius) {   
  -webkit-border-radius: $radius;   
     -moz-border-radius: $radius;   
      -ms-border-radius: $radius;   
          border-radius: $radius;   
}   
.box { @include border-radius(10px); }

---

Мат. функции   
можно использовать `+` `-` `*` `/`   
а так же `%` - (100%)

---

if & @if   
`if ()` - работает так же как в языках программирования   
`@if` - добавляет стили только если данный @if возвращает true

Пример

`@if 5 < 3` - { border: 2px dotted; } сработает   
`@if null` - { border: 3px double; } не сработает

---

@for   
`@for $i from 1 through 3` - цикл на 3 повторения

---

@each   
@each $animal in puma, sea-slug, egret, salamander {   
  .#{$animal}-icon {   
    background-image: url('/images/#{$animal}.png');   
  }   
}   

применить для всех элементов

---

@while   
`@while $i > 0` - цикл пока не выполнится условие   

---

@functions   
@function grid-width($n)   
{   
 code   
 @return   
}   

`@return` - обязателен