# GR_3371
# Инструкция по работе с Git

## Что такое git

**Git** - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.


## Подготовка репозитория

Для создание репозитория необходимо выполнить команду *git init* в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)


## Создание сохранений

Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

Команда *git diff* используется для вычисления разницы между любыми двумя **Git** деревьями. Это может быть разница между вашей рабочей директорией и индексом (собственно *git diff*), разница между индексом и последним коммитом (*git diff --staged*), или между любыми двумя коммитами (*git diff master branchB*).

Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ДОБАВЛЕНЫ и сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**.

## Перемещение между сохранениями

Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## Журнал изменений

Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Ветки в git

Для того, чтобы создать ветку, используется команда git branch. Делается это следующим образом в папке с репозиторием: git branch <название новой ветки>

## Слияние веток и решение конфликтов

Для того чтобы дабавить ветку в текущую ветку используется команда *git merge*

При работе в двух ветках одновременно может
возникнуть ситуация, когда в одной и другой
ветке мы по-разному изменили блок текста.
Если затем мы попробуем слить эти ветки, Git
сообщит о конфликте и предложит выбрать,
какие же изменения записать.

## Удаление веток

Для удаления ветки ввести команду "git branch -d 'name branch'"

## Получение справки

Для получения справки прописываем (--help) в конце. Например  git --help ,  git log --help , git commit --help

## Работа с удаленными репозиториями.

Копировать внешний репозиторий на свой ПК можно командой *git clone.*
Команда *git clone* составная: она не только
загружает все изменения, но и пытается слить
все ветки на локальном компьютере и в
удаленном репозитории.

## git pull

Эта команда позволяет скачать все
из текущего репозитория и автоматически
сделать merge с нашей версией

## git push

Отправить свою версию репозитория во
внешний репозиторий поможет команда *git
push*. При первом её использовании нужна авторизация.

## pull request

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают
команду *pull request*. Предлагать изменения на **GitHub** нужно в отдельной ветке. Сначала
пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет
изменения командой *push* в свой аккаунт на **GitHub** и даёт команду *pull request*. 