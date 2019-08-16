## Разработка темы для WP

Клонируем репозиторий  

В папку проекта ставим [Wordpress](https://wordpress.org/download/)  

Далее читаем [README.md](https://github.com/andreysuha2/wp-start-theme/tree/master/wp-content/themes/wordpress-starter-theme) темы  

## Работа с гит

Папки и файлы WP в гитигноре  

Для удобства установленные плагины будут храниться в репозитории  

## Настройка проекта

домен для разработки: `example.local`  

префикс для таблиц: `wp_`  




Старт проекта Wordpress Themes:
После того как вы в консоле перешли в папку с проектами, далее нужно клонировать стартовый проект:
git clone https://github.com/andreysuha2/wp-start-theme domain-name
параметр domain-name переименуйте на свой домен для разработки.

В созданную папку ставим Wordpress перед установкой почитать установка и настройка WP

Обязательно активируем чекбокс “Discourage search engines from indexing this site”(после установки, активировать возможно, перейдя Settings - Reading - Search Engine Visibility).


Переименовываем название папки темы на название проекта и в style.css темы тоже меняем название

Переходим в папку с проектом в консоле:
cd domain-name

далее выполняем ряд команд:
rm -rf .git
удалить папку гита стартового проекта (эта команда работает на линуксе или в cmder)
для windows использовать команду rd /s /q ".git"

git init
инициируем гит для нового проекта

git add .
добавим стартовый проект в гит нового проекта

git commit -m "init"
создаем коммит инициализации

git remote add origin адрес созданного репозитория
добавляем адрес удаленного репозитория
пример: git remote add origin https://nickname@bitbucket.org/f5-team/repo.git

git push -u origin master
заливаем первый коммит на битбакет и назначим по умолчанию ветку мастер

Как работать с стартовым проектом - читаем README.md стартового проекта в данном случае здесь - https://github.com/andreysuha2/wp-start-theme

Внимание!
Не заходите в админку через localhost только через домен.
Не заливайте папку node_modules на сервер! Исключите ее перед созданием архива.
После разработки темы и переноса на продакшн деактивируем чекбокс Discourage search engines from indexing this site (Settings - Reading - Search Engine Visibility).
