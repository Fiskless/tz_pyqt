# Телефонная книга

В данном проекте создана телефонная книга.

## Как запустить локально

- Скачайте код
- Установите зависимости командой `pip install -r requirements.txt`
- В данном проекте используется база данных mariadb. Соответсвенно необходимо пользователя БД и саму базу данных с названием 'phone_book'. 
- Для запуска используйте команду `python main.py`

## Переменные окружения

Часть настроек проекта берётся из переменных окружения. Чтобы их определить, создайте файл `.env` рядом с `main.py` и запишите туда данные в таком формате: `ПЕРЕМЕННАЯ=значение`.

Доступны 3 переменные:
- `USER` — имя вашего пользователя для входу в базу данных
- `PASSWORD` — ваш пароль для входа в базу данных

## Руководство по пользованию 

Когда пользователь запускает программу перед ним появляется окно авторизации.При включенном чекбоксе – «Запомнить меня» и успешном входе, при закрытии программы и повторном запуске будет автоматический вход без авторизации. Чтобы сменить пользователя необходимо нажать кнопку "Выйти", и тогда откроется окно авторизации.

![Image alt](https://github.com/Fiskless/tz_pyqt/blob/main/pictures/login_window.png)

Пользователь вводит логин и пароль, нажимает кнопку «Войти». В случае нахождения пользователя с такой комбинацией программа переходит к главному меню, в случае отсутствия появляется всплывающее окно «Пользователь с такими данными не найден»

![Image alt](https://github.com/Fiskless/tz_pyqt/blob/main/pictures/login_window.png)

Если пользователь забыл пароль – по нажатию на ссылку «Забыли пароль?» открывается окно «Восстановление пароля»

![Image alt](https://github.com/Fiskless/tz_pyqt/blob/main/pictures/password_reset_window.png)

При нажатии на кнопку «Регистрация» открывается окно «Регистрация»

![Image alt](https://github.com/Fiskless/tz_pyqt/blob/main/pictures/new_user_window.png)

В случае успешного входа/регистрации перед пользователем открывается главное окно с навигацией по Алфавиту.
Также реализована система напоминаний: при открытии программы открывается окно, в котором показывается список именинников на ближайшую неделю.

![Image alt](https://github.com/Fiskless/tz_pyqt/blob/main/pictures/birthday_reminder.png)

Есть возможность добавления, редактирования, удаления контакта. Для этого используются кнопки "Добавить", "Обновить", "Удалить". 
В программе есть логический контроль дубликатов, то есть запрет на создание пользователя с данными, которые полностью совпадают с существующим контактом.


