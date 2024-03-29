# Инструкция по работе с Git-ом

## Что такое GIT?
Git - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте.

## Подготовка репозитория
Для создания репозитория необходимо выполнить команду

> *git init*

В папке с репзиторием появится скрытая папка *.git*

## Создание коммитов

### Команда git add

Для добавления изменений в коммит используется комманда:

>*git add .*

Она позволит добавить все изменения, если есть потребность добавить только некоторые файлы, то необходимо использовать команду:

>*git add <Имя ФАЙЛА>*

### Состояния репозитория

Состояние репозитория можно посмотреть, использовав команду:

>*git status*

Команда покажет (возможные) изменения в файлах

### Коммит

Чтобы зафиксировать изменения перед отправкой файлов на ветку необходимо выполнить команду:

>*git commit -m "Сообщение"*

### Push изменений
Чтобы отправить все необходимые изменения на ветку после закрепления коммитом необходимо выполнить комманду:

>*git push origin main*

### Ветки
Чтобы посмотреть какие ветки созданы нами в репозитории, необходимо выполнить команду:

>*git branch*

Чтобы создать новую ветку, необходимо выполнить команду:

>*git checkout -b <ИМЯ ВЕТКИ>*

Чтобы перейти в нужную нам ветку, необходимо выполнить команду:

>*git checkout <ИМЯ ВЕТКИ>*

### Логирование
Чтобы посмотреть информацию о совершенных действиях разработчиком можно ввести команду:

>*git log*

### Работа с удалёнными репозиториями

Для того, чтобы внести вклад в какой-либо Git-проект, вам необходимо уметь работать с удалёнными репозиториями. Удалённые репозитории представляют собой версии вашего проекта, сохранённые в интернете или ещё где-то в сети. У вас может быть несколько удалённых репозиториев, каждый из которых может быть доступен для чтения или для чтения-записи. Взаимодействие с другими пользователями предполагает управление удалёнными репозиториями, а также отправку и получение данных из них. Управление репозиториями включает в себя как умение добавлять новые, так и умение удалять устаревшие репозитории, а также умение управлять различными удалёнными ветками, объявлять их отслеживаемыми или нет и так далее. В данном разделе мы рассмотрим некоторые из этих навыков.

### Просмотр удалённых репозиториев

Для того, чтобы просмотреть список настроенных удалённых репозиториев, вы можете запустить команду git remote. Она выведет названия доступных удалённых репозиториев. Если вы клонировали репозиторий, то увидите как минимум origin — имя по умолчанию, которое Git даёт серверу, с которого производилось клонирование

![Пример](1.png)

### Добавление удалённых репозиториев
 Для того, чтобы добавить удалённый репозиторий и присвоить ему имя (shortname), просто выполните команду:
 
 >*git remote add shortname url*

 ### Получение изменений из удалённого репозитория — Fetch и Pull

Для получения данных из удалённых проектов, следует выполнить:

>*git fetch [remote-name]*

### Отправка изменений в удалённый репозиторий (Push)

Когда вы хотите поделиться своими наработками, вам необходимо отправить их в удалённый репозиторий. Команда для этого действия простая: git push [remote-name] [branch-name]. Чтобы отправить вашу ветку master на сервер origin (повторимся, что клонирование обычно настраивает оба этих имени автоматически), вы можете выполнить следующую команду для отправки ваших коммитов:

>*git push origin master*

### Просмотр удалённого репозитория

Если хотите получить побольше информации об одном из удалённых репозиториев, вы можете использовать команду git remote show remote

### Удаление и переименование удалённых репозиториев

Для переименования удалённого репозитория можно выполнить git remote rename