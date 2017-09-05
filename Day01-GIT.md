# GIT

## Что такое GIT?

Git это
* система контроля версий
* свободное программное обеспечение 
* хранилище кода (это в первую очередь, но вообще-то любых файлов)

Есть и другие подобные системы, например, Mercurial или SVN. Но мы пользуемся Git, потому что это один из самых популярных в IT-сообществе. А раз популярный, то для него сделано много полезного разными людьми. Например, благодаря одному из таких инструментов можно делать мультики из истории изменений:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=7Klex2I08JU" target="_blank"><img src="http://img.youtube.com/vi/7Klex2I08JU/0.jpg" 
alt="commits vizual" width="240" height="180" border="10" /></a>

## Зачем нам это нужно?

Нужно для того чтобы

* Иметь доступ к истории разработки (кто, когда, что написал) <br>
                если еще вчера ваша программа работала верно, а сегодня все сломалось, то достаточно взглянуть, какие изменения вы внесли в код за прошедшую ночь :) и (возможно) все откатить
* Распределять права доступа к совместному коду (кому можно его редактировать, а кому - только смотреть)
* Параллельно разрабатывать несколько версий программы
* Разрабатывать в команде: чтобы у всех участников проекта на компьютере оказывался один и тот же код

[Видео Зачем программисту профиль на GitHub?](https://www.youtube.com/watch?v=WFFAUyomZBk)

## Как работает git?

Вы скачиваете на компьютер специальную программу git-клиент и говорите ей, в какой директории (~папке на компьютере) нужно отслеживать изменения. Это ваш *локальный репозиторий*.

Еще вы можете сохранить ваши файлы в *удаленном репозитории* - на каком-то веб-сервисе в Интернете. Теперь вы можете хранить ваш код где-то в облаке, иметь к нему доступ отовсюду, синхронизировать ваш код на компьютере и удаленный репозиторий и делиться кодом с друзьями =) 

Когда вы вносите изменения, вы отправляете их на удаленный репозиторий. А когда ваши друзья-разработчики хотят что-то добавить, они сначала скачивают ваши изменения, затем вносят свои и тоже отправляют их в удаленный репозиторий.

## Как этим пользоваться?

### Шаг 1

Сначала нужно зарегистрироваться на [GitHub](https://github.com/). GitHub - это такой сервис в интернете для хостинга репозиториев. Бывают и другие. Но GitHub самый авторитетный, густонаселённый и удобный (хотя бы [куча всяких статистик](https://github.com/maryszmary/adj_and_ngramms/graphs/punch-card), по которым видно, когда и во сколько студенты занимаются своими курсовыми :) но это не все [плюсы гитхаба](https://habrahabr.ru/company/2gis/blog/306166/)). А ещё бесплатный для тех репозиториев, которые вы готовы показать миру.

### Шаг 2
Теперь нужно скачать программу git-клиент. <br>
Вы можете скачать программу с графическим интерфейсом (с окошками и кнопками), например, [SmartGit](http://www.syntevo.com/smartgit/) или выбрать что-то вот [здесь](https://git-scm.com/downloads/guis). Такой программой пользоваться проще.<br>
Или вы можете скачать консольную версию (т.е. командную строку с черным окошком и текстовым кодом, когда вы пользуетесь такой штукой, все думают, что вы хакер!). Например, [git-scm](https://git-scm.com/downloads). Такой программой пользоваться чуть-чуть сложнее.
Прежде всего, нужно создать свой репозиторий. Сделать это удобно на самом github'е, [нажав на плюсик](https://github.com/new) в правом верхнем углу окна. После этого запишите, пожалуйста, ссылку на свой репозиторий в [форму](https://goo.gl/forms/m24dN2hTQwQdtkuC3), чтобы мы знали, где искать ваши домашки.

#### Если вы скачали SmartGit
1. Скопируйте git-ссылку на ваш удаленный репозиторий (это не то же самое, что вы видите в адресной строке браузера).

![clone](https://github.com/ElizavetaKuzmenko/Programming-and-computer-instruments/blob/master/images/clone.png)

2. В SmartGit откройте пункт меню Repository -> Clone и скопируйте туда эту ссылку.

3. Вносите изменения в файлы.

4. Нажмите кнопку Commit в верхнем меню, чтобы зафиксировать изменения.

5. Нажмите кнопку Push, чтобы внести изменения и в удалённый репозиторий.

6. При необходимости синхронизировать локальный репозиторий с удалённым, нажмите кнопку Pull в верхнем меню.

#### Если вы решили пользоваться консолью 
1. Скопируйте git-ссылку на ваш удаленный репозиторий (это не то же самое, что вы видите в адресной строке браузера).
2. Откройте консоль и перейдите в любую симпатичную вам папку с помощью команды `cd` (например, `cd 'Мои Документы'`, cd = change directory). В консоли напишите `git clone <git-ссылка>`. На вашем компьютере появится локальный репозиторий со всеми файлами, которые лежали в удалённом.
3. Установите отслеживание ваших файлов, выполнив в консоли команду `git add .`
4. Работайте на своём компьютере, меняйте содержание файлов, удаляйте их, добавляйте новые.
5. Зафиксируйте произошедшие изменения, выполнив в консоли команду `git commit -m <message>`. Вместо `<message>` нужно написать что-нибудь осмысленное, чтобы и спустя полгода вы могли вспомнить, какие изменения внесли.
6. Синхронизируйте ваш локальный и удалённый репозитории с помощью команды `git push`. Введите имя пользователя и пароль. Все ваши изменения появятся на гитхабе.
7. Если вы работали на другом компьютере или ваши товарищи изменяли файлы в удалённом репозитории, синхронизировать удалённый и локальный репозитории можно с помощью команды `git pull`.
7. Разрешить людям редактировать ваш код можно в настройках репозитория.

![collaborators](https://github.com/ElizavetaKuzmenko/Programming-and-computer-instruments/blob/master/images/collab.png)

#### А ещё, если совсем-совсем ничего не получается,

а дедлайн наступает, можно воспользоваться веб-интерфейсом для загрузки файлов в репозиторий (а настоящие хакеры называют его просто _реп_)

## Также можно посмотреть...
* [Очень хороший курс](https://geekbrains.ru/courses/66) по работе с git. Будете знать всё и даже гораздо больше.
* [Обучающая компьютерная игра](https://www.git-game.com/), которая поможет приобрести хорошие навыки в работе с git через консоль.
* [Малоизвестные команды git](https://habrahabr.ru/company/mailru/blog/318508/).