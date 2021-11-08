# Оформление кейсов topdg

### Файловая структура

*  /
   *  [НазваниеКейса].html
*  /images/
   *  [НазваниеКейса-[экран]__[НазваниеКартинки]].[расширение]
*  /js/
   *  [НазваниеКейса].js
*  /scss/
   *  [НазваниеКейса].scss
*  /fonts/
   *  /[НазваниеШрифта]/

### Технологии

1. JS (Vanila)
2. SCSS
3. Без JQuery и CSS фреймворков

### Структура HTML

* Нейминг - [BEM-методология](https://ru.bem.info/) или ей подобная
  * .case
    * section.case__section-[id]
      * .container - опционально
        * h2.case__section-[id]__title
        * img.case__section-[id]__img
        * .case__section-[id]__content
        * .case__section-[id]__items
          * .case__section-[id]__item
          * .case__section-[id]__item_title
          * .case__section-[id]__img
          * и т.д. и т.п.
* [Пример](./jarina.html)
* Используемые переменные (файл [vars.css](./scss/vars.scss))

### Структура SCSS
* Файл
```
.case {
   &__section-[id]{
      &__title{

      }
      &__img{

      }
   }   
}
```
* В случае подключения сторонних вещей @import укащываем в начале файлай 
* [Пример](./scss/jarina.scss)

### Работа с JS
* библиотеки подключаем в файле кейса в начале документа через import
* Используемые сейчас: package.json 
` 
"dependencies": {
   "@babel/polyfill": "^7.12.1",
   "particles.js": "^2.0.0",
   "simplebar": "^5.3.6",
   "swiper": "^6.4.1",
   "swup": "^2.0.13",
   "vivus": "^0.4.6"
} 
`