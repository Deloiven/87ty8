# Продвинутое программирование на PHP — Laravel

 Критерии оценки работы:

>Принято: **
— выполнены все пункты задания;
— в работе используются указанные инструменты и соблюдены условия;
— код корректно отформатирован по стандартам программирования на PHP;
— скрипт запускается, выводит различные данные на экран, не вызывает ошибок.
> 
>**На доработку:
— выполнены не все обязательные пункты задания;
— задание выполнено с ошибками.
___
## Урок 1. Введение, установка и первичная настройка
1. Установите PHP на компьютер. Для этого вы можете скачать PHP с официального сайта или развернуть образ Docker с PHP. Наиболее простой способ, рекомендуемый для выполнения этого задания, — воспользоваться сборкой XAMMP. Скачать сборку для вашей платформы можно на сайте Apache Friends.

2. Откройте утилиту командной строки в своей операционной системе.

3. Выполните команду php -v и убедитесь, что PHP работает.

4. Установите Composer. Выполните необходимые команды, описанные на официальном сайте.

5. Установите Laravel с помощью Composer. Выполните команду composer create-project laravel/laravel <имя проекта>, где имя проекта — это имя вашего проекта. Этому имени будет соответствовать имя папки, куда будет помещён проект.

6. Перейдите в папку, соответствующую имени проекта.

7. Убедитесь, что папка не пустая, и выполните команду php artisan serve --port=8080. Эта команда запустит встроенный веб-сервер Laravel.

8. Откройте браузер и перейдите по адресу http://localhost:8080. Если всё работает правильно, вы увидите страницу с информацией о фреймворке Laravel.

9. Сделайте скриншот.\



___
[Решение](https://# "Домашнее задание - решение")

MySQL в контейнере
```
docker compose up -d
```

![Изображение](./homework/1/1.png "Домашнее задание - решение")

![Изображение](./homework/1/2.png "Домашнее задание - решение")

___

## Урок 2. Контроллеры, экшены и роутинг
1. Установите Laravel с помощью composer, выполнив команду composer create-project laravel/laravel <имя проекта>. В поле <имя проекта> впишите имя вашего проекта. Этому имени будет соответствовать имя папки, в которую вы поместите проект.

2. Создайте контроллер для вывода формы на страницу и её обработки. В командную строку введите команду php artisan make:controller FormProcessor.

3. После выполнения команды убедитесь, что контроллер создан, — соответствующий файл должен появиться в папке app/Http/Controllers.

4. Внутри контроллера опишите метод index: он должен выводить в браузер форму для заполнения.
   — Опишите форму в виде шаблона blade.
   — Внутри формы должны быть поля для ввода имени, фамилии и email пользователя.
   — Форма отправляется методом POST.
   — Параметр action пока оставьте пустым.
   — Не забудьте про CSRF.

5. Внутри файла /routes/web.php опишите новый роут (метод GET), который будет вызывать метод index контроллера FormProcessor по url /userform.

6. Запустите встроенный сервер Laravel командой php artisan serve --port=8080 и убедитесь, что форма выводится по адресу http://localhost:8080/userform.

7. В контроллере FormProcessor создайте метод store для обработки формы. Этот метод должен принимать поля формы и отправлять ответ в виде JSON-объекта, содержащего значения полей формы (имя, фамилия, email).

8. Внутри файла /routes/web.php опишите новый роут (метод POST), который будет вызывать метод store контроллера FormProcessor по url /store_form.

9. Отредактируйте поле action формы в шаблоне и укажите адрес /store_form.

10. Откройте форму в браузере по адресу http://localhost:8080/userform, заполните её и попробуйте отправить на сервер, нажав кнопку Submit. Если всё сделано правильно, вы увидите в браузере объект JSON.

11. Создайте новый шаблон blade для приветствия пользователя (например: «Привет, <имя>!»).

12. Измените метод store контроллера FormProcessor таким образом, чтобы вместо JSON он возвращал шаблон, заполненный данными пользователя.

13. Сделайте коммит своих изменений с помощью git и отправьте push в репозиторий.



#   8 7 t y 8  
 