.7 Практическая работа
В этом модуле мы:

познакомились с понятием жизненного цикла;
узнали, из каких этапов обычно состоит жизненный цикл;
рассмотрели две модели жизненного цикла;
познакомились с инструментом Maven;
научились настраивать плагины и репозитории Maven;
узнали, что такое docker и как им управлять;
научились выполнять HTTP-запросы с помощью Postman.
Закрепите полученные знания, выполнив практические задания. Все задания обязательны для выполнения.



Цели домашнего задания
Научиться: 

самостоятельно настраивать плагины Maven и добавлять репозитории;
создавать и запускать docker-compose файл;
выполнять запрос Postman.
Домашние задания этого модуля необходимо сдавать через систему контроля версий Git. Для этого ознакомьтесь с инструкцией, разделы «Начало работы» и «Сдача домашних заданий».



Задание 1
Что нужно сделать

Настройте плагин проверки стиля кода в проекте Maven. Для этого создайте новый проект Maven (название проекта не важно). Добавьте плагин checkstyle. Настройте запуск проверки до этапа компиляции проекта.

Параметры плагина:

groupId: org.apache.maven.plugins
artifactId: maven-checkstyle-plugin
version: 3.0.1-SNAPSHOT
Цель, которая запускает проверку: check.

Адрес репозитория SNAPSHOT.



Критерии оценки

Зачёт: при запуске теста проекта выполняется проверка плагином checkstyle версии 3.0.1-SNAPSHOT.





Задание 2
Что нужно сделать

Добавьте в проект, созданный в предыдущем задании, файл docker-compose.yaml.

Настройте запуск сервиса базы данных MySQL, чтобы база была доступна по порту 9977 и подключалась под пользователем testuser и паролем testpassword. 

Входные данные:

докер-образ: mysql;
версия: не важна;
порт, на котором запускается MySQL: 3306;
пароль и логин настраивается через переменные окружения: MYSQL_USER, MYSQL_PASSWORD.


Критерии оценки

Зачёт: база запускается с помощью docker-compose и доступна по порту 9977 с подключением по testuser/testpassword.



Задание 3
Что нужно сделать

Создайте коллекцию запросов поиска работы в Postman.

В коллекции должно быть три запроса, разделённых по языкам программирования Java, Python, Ruby. Поиск производите по адресу.

Запросы должны делаться для двух городов:

moscow;
new+york. 


Метод запроса GET. 

Параметры запроса:

description: язык программирования;
location: город.


Важные условия:

Города переключаются через переменные в environment postman.
Базовая часть адреса должна быть в переменной коллекции. 


Коллекцию экспортируйте и положите в репозиторий проекта из предыдущих задач.



Критерии оценки

Зачёт: запросы из коллекции выполняются, в них учтены важные условия.
