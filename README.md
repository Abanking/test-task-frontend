![Cover](https://user-images.githubusercontent.com/57585370/209634490-bb2b956e-f0eb-49c8-99aa-d08182b4f29a.jpg)

# Тестовое задание на позицию Junior Frontend Developer

## Содержание
1. [Требования](#requirements)
2. [Требования к верстке](#requirements-html)
3. [Если вы Open Source Contributor](#opensource)
4. [Задача](#task)

## Требования <a name="requirements">
1. Использование чистого JS/TS, либо Angular (14 версии либо выше)
2. Все формы должны быть реализованы с использованием ReactiveForm, если используется Angular

## Требования к верстке <a name="requirements-html">
1. Нельзя использовать фреймворки типа bootstrap
2. Запрещено использовать !important
3. Используйте БЭМ (необязательно)

## Если вы Open Source Contributor <a name="opensource">
Если у вас есть свои проекты с открытым исходным кодом или вы активно вносите свой вклад в разработку популярных библиотек, то 
напишите на почту .... Тестовое задание делать не нужно

## Задача <a name="task">
Вам нужно реализовать приложение, которое отображает список компаний, детальную информацию о компании, а также расположение компании на карте.

### Авторизация
На данной странице пользователь вводит логин/пароль, который сохраняется в local storage. Если в local storage нет информации о логине или пароле, то пользователь считается неавторизованным и он не должен иметь возможности попасть на любой другой роут веб-приложения. Если пользователь авторизован и заходит на страницу авторизации, то его нужно перенаправлять на страницу со списком компаний.

### Список компаний
Для получения списка компаний нужно использовать рест `https://random-data-api.com/api/company/random_company`. Query параметром size можно передать количество требуемых компаний
Нужно, как минимум, отображать логотип, название, вид деятельности и тип
Также должна быть возможность сортировки списка по названию, виду деятельности и типу
  
Дополнительно:
  
1. Реализовать кеширование запроса в рамках сессии
2. Реализовать ленивую подзагрузку данных. Сначала мы получаем n количество компаний, когда долистываем до вершины списка, то происходит дозапрос компаний

### Детальная информаци о компании
При нажатии на компанию в списке мы должны попасть на страницу с детальной информацией о компании. На странице нужно отображать логотип, название, вид деятельности, слоган, контактный номер телефона, адрес.
  
Дополнительно:
  
На этой странице должна располагаться карта (можно использовать любой API). На карте должно быть отмечено расположение компании

### Добавление компании
На данную страницу можно перейти со страницы списка компаний. Страница представляет из себя форму, где пользователь заполняет
- название компании (обязательное поле, не более 15 символов)
- вид деятельности (селект: лесоводство и лесозаготовки, добыча угля, производство мебели, научные исследования и разработки, деятельность общественных организаций. Обязательный выбор)
- присутствие на Российском рынке (чекбокс)
  
При сохранении формы должен генерироваться JSON (нужно написать его в консоли), а далее происходить редирект на страницу со списком компаний


