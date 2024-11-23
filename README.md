# Лабораторная работа №6, "Github"

## 1 Цель работы
Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

## 2 Ход работы

## 3 Лог команд
```bash
git config --global --edit
git config --global --edit

git clone https://github.com/RomanPro100/LR6
code LR6
git pull
git log --all --graph

git add mergefile.txt
git commit -m "Решил конфликт слияния"

git push origin master --delete origin/branch1
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
## 4 Скриншоты

## 5 Выводы