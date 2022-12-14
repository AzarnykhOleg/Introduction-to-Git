# **Инструкция по работе с Git**

![котик](cat.jpg)

## Предварительная настройка Git

Чтобы "представиться" программе Git нужно ввести команды:

    git config --global user.name "ваше_имя"
    git config --global user.email "адрес_почты@email.com"

## Создание репозитория

Чтобы инициализировать новый репозиторий нужно ввести команду:

    git init

## Добавление в индекс

Чтобы добавить изменения в индекс (для фиксации в следующем коммите) нужно ввести команду:

    git add <имя_файла>

## Запись индексированных изменений в репозиторий (коммит)

Чтобы зафиксировать изменения, добавленные в индекс, нужно ввести команду:

    git commit

Чтобы закомментировать коммит прямо из командной строки вместо текстового редактора нужно ввести команду:

    git commt -m "комментарий к коммиту"

Чтобы совершить коммит, автоматически индексируя изменения в файлах проекта, нужно ввести команду:

    git commit -a

Чтобы закомментировать коммит прямо из командной строки вместо текстового редактора, автоматически индексируя изменения в файлах проекта, нужно ввести команду:

    git commt -am "комментарий к коммиту"

## Получение информации о коммитах

Чтобы получить справку по всем коммитам, коснувшимся активной в настоящий момент ветки, нужно ввести команду:

    git log

Чтобы получить подробную информацию о каждом в виде патчей по файлам из коммитов нужно ввести команду:

    git log -p

Чтобы получить информацию о каждом из коммитов по строчке, состоящей из хэша, нужно ввести команду:

    git log --oneline

Чтобы получить подробную информацию о каждом из коммитов во всех ветках нужно ввести команду:

    git log --all

Чтобы получить подробную информацию о каждом из коммитов во всех веткахпо строчке, состоящей из хэша, нужно ввести команду:

    git log --all --oneline

## Поиск отличий между деревьями проекта, коммитами, состоянием индекса и каким-либо коммитом

Чтобы просмотреть изменения, не внесенные в индекс, нужно ввести команду:

    git diff

Чтобы просмотреть различия двух коммитов, определяя их по хэшам нужно ввести команду:

    git diff <hash_1_commit> <hash_2_commit>

## Переключение между ветками, извлечение отдельных файлов из истории коммитов

Чтобы перейти к коммиту по его хэшу нужно ввести команду:

    git checkout <hash_commit>

Чтобы вернуться (перейти) в ветку master нужно ввести команду:

    git checkout master

## Состояние проекта, измененные и не добавленные файлы, индексированные файлы

Чтобы получить информацию обо всех изменениях, внесенных в дерево директорий проекта нужно ввести команду:

    git status

## Игнорируемые файлы

Игнорируемый файл — файл, явным образом помеченный для Git как файл, который необходимо игнорировать (как правило, артефакты сборки и файлы, генерируемые машиной из исходных файлов в  репозитории, либо файлы, которые по какой-либо иной причине не должны попадать в коммиты).
***
Игнорируемые файлы отслеживаются в специальном файле .gitignore, который регистрируется в корневом каталоге репозитория. В Git нет специальной команды для указания игнорируемых файлов: вместо этого необходимо вручную отредактировать файл .gitignore, чтобы указать в нем новые файлы, которые должны быть проигнорированы. Файлы .gitignore содержат шаблоны, которые сопоставляются с именами файлов в репозитории для определения необходимости игнорировать эти файлы.

## Ветвление в Git

Git branching, или ветвление Git – способ работать над приложением и одновременно отслеживать его версии.
***
Ветвь разработки – это бифуркация состояния кода, создающее новый путь для его эволюции; возможность генерировать разные ветки Git, которые будут существовать параллельно к главной ветке. Таким образом, возможно упорядоченно и точно включать новые функции в разрабатываемый код.

## Перемещение между ветками в Git

Для перемещения между между ветками в Git необходимо ввести команду:

    git checkout <название_необходимой_ветки>

## Конфликты слияния веток

 [О конфликтах слияния веток и их разрешении подробнее](https://habr.com/ru/post/323234/ "Хабр")

## Удаление веток в Git

Для удаления ветки в Git необходимо ввести команду:

    git branch -d <название_удаляемой_ветки>

Для безусловного удаления ветки в Git необходимо ввести команду:

    git branch -D <название_удаляемой_ветки>

## Создание веток

Для создания новой ветки в Git нужно ввести команду:

    git branch <название_новой_ветки>

## Вывод дерева зависимостей в графическом виде

Для вывода дерева зависимостей для всех коммитов в графическом виде надо выполнить команду:

    git log --graph

## Слияние веток

Мердж или слияние веток - это перенос кода из одной ветки в другую.
Для добавления (слияния) информации (кода) ветки "ветка_2" в "ветку_1" необходимо, находясь в "ветке_1", выполнить команду:

    git merge "ветка_2"
