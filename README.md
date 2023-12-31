# Завершающая лабораторная по веб проектированию
Основная цель данной лабораторной работы – научиться обрабатывать веб-формы на стороне приложения, освоить инструменты, которые предоставляет Django, по работе с формами. Также в этой лабораторной работе вы освоите инструменты Django по
работе с авторизацией и реализуете простейшую авторизацию. Напоследок, вы познакомитесь с инструментом администрирования Django – как в несколько строчек кода сделать панель администратора сайта.
---
1. Создайте view, которая возвращает форму для регистрации.
Поля формы:
* Логин
* Пароль
* Повторный ввод пароля
* Email
* Фамилия
* Имя
2. Создайте view, которая возвращает форму для авторизации.
Поля формы:
* Логин
* Пароль
3. При отправке формы регистрации во view проверять каждый параметр по
правилам валидации, если валидация всех полей пройдена, то создавать
пользователя и делать перенаправление на страницу логина, а ошибки,
если они есть, выводить над формой.
Правила валидации:
* Логин не меньше 5 символов
* Пароль не меньше 8 символов
* Пароли должны совпадать
* Все поля должны быть заполнены
* Логин – уникален для каждого пользователя
4. При возникновении ошибок в момент отправки формы, введенные
значения в полях ввода, кроме пароля, не должны исчезать.
5. Переписать view регистрации с использованием Django Form, правила
валидации удалить из view, использовать встроенный механизм
валидации полей.
6. Во view авторизации реализовать логин при POST запросе. При успешной
авторизации должен происходить переход на страницу успешной
авторизации.
7. Страница успешной авторизации должна проверять, что пользователь
авторизован. Иначе делать перенаправление на страницу авторизации.
8. Реализовать view для выхода из аккаунта.
9. Заменить проверку на авторизацию на декоратор login_required
10. Добавить superuser’a через комманду manage.py
11. Подключить django.contrib.admin и войти в панель администрирования.
12. Зарегистрировать все свои модели в django.contrib.admin
13. Для выбранной модели настроить страницу администрирования:
* Настроить вывод необходимых полей в списке
* Добавить фильтры
* Добавить поиск
* Добавить дополнительное поле в список
