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

### 2.3 Создание и подтягивание файла
В интерфейсе Github в ветку `master` был добавлен текстовый файл.

![](screens/05_creating_file.png)

![](screens/06_creating_file2.png)

После этого в локальном репозитории были получены изменения в удалённом репозитории при помощи команды `git pull`.

![](screens/07_pulling.png)

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