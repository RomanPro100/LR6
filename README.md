# Лабораторная работа №6, "Github"

## 1 Цель работы
Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

## 2 Ход работы
Работа проводилась на ОС Linux Mint 22, в котором по умолчанию установлен `git`, с использованием редактора VS Code.

### 2.1 Настройка клиента
На момент начала работы аккаунт на Github [уже был создан](https://github.com/RomanPro100), но необходимо было настроить локальный клиент Git. Глобальные настройки Git в Linux хранятся в файле `~/.gitconfig`, его можно отредактировать командой `git config --global --edit`. Получить отдельные настройки можно командой `git config --global <название_настройки>`, а изменить — командой `git config --global <название_настройки> <новое_значение>`.

![](screens/01_git_config.png)

![](screens/02_configured_name.png)

### 2.2 Клонирование репозитория
После этого в интерфейсе Github был создан форк [репозитория](https://github.com/Kurtyanik/LR6) с копированием всех веток, [сам форк](https://github.com/RomanPro100/LR6) был клонирован на устройство командой `git clone`.

![](screens/03_forked_repo.png)

![](screens/04_cloning.png)

После клонирования репозиторий был открыт для дальнейшей работы в редакторе VS Code командой `code LR6`.

### 2.3 Создание и подтягивание файла
В интерфейсе Github в ветку `master` был добавлен текстовый файл `a.txt`.

![](screens/05_creating_file.png)

![](screens/06_creating_file2.png)

После этого в локальном репозитории были получены изменения в удалённом репозитории при помощи команды `git pull`.

![](screens/07_pulling.png)

В проводнике можно увидеть подтянутый файл.

![](screens/08_file_in_explorer.png)

### 2.4 Просмотр истории изменений

Просмотреть историю коммитов во всех ветках в виде графа можно при помощи команды `git log --all --graph`.

![](screens/09_commit_history.png)

Ещё в VS Code есть вкладка Source Control, в которой можно просматривать историю коммитов в разных ветках, изменения файлов, добавлять файлы в индекс.

![](screens/10_vsc_source_control.png)

### 2.5 Устранение конфликта слияния

В VS Code при возниканиии конфликта слияния конфликтующие файлы отмечены прямо в проводнике, и если их открыть, можно увидеть конфликтующие строки.  

![](screens/11_merge_conflict.png)

Сверху перечислены опции, как решить конфликт. В данном случае был выбран вариант `Accept Current Change`, т.е. оставить файл таким, какой он есть в ветке `master` и проигнорировать изменения в ветке `branch1`.

Затем необходимо было добавить файл в индекс и сделать коммит. После этого ветки автоматически слились, и таким образом конфликт слияния был решён.

![](screens/12_resolving_conflict.png)

Изменения видны и во вкладке Source Control в VS Code: можно увидеть, как две ветки слились в одном коммите.

![](screens/13_after_resolve.png)

## 3 Лог команд
```bash
git config --global --edit

git clone https://github.com/RomanPro100/LR6
code LR6
git pull
git log --all --graph

git add mergefile.txt
git commit -m "Решил конфликт слияния"

git push origin master --delete branch1
git push origin master
git branch -D branch1

git add a.txt
git commit -m "Добавил больше букв"
git add a.txt
git commit -m "Добавил ещё букв"
git revert HEAD

git branch otchet
git switch otchet
```
## 4 История операций

## 5 Выводы