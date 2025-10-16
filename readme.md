1. Создал новый репозиторий на гитхаб
Он пустой, ничего не клонировал, просто сделал из инструкции на странице репозитория в гитхабе

git init
git remote add origin https://github.com/Blikir13/HSE_MS_Theme3_github.git

2. nano main.py
чето написать
НЕ ЗАБУДЬТЕ СОЗДАТЬ ГИТИГНОР С .DS_Store

git add .
git commit -m "initial commit"
git push --set-upstream origin master

3. git checkout -b develop

nano main.py - изменить чето

git add .
git commit -m "Добавлены изменение какие-то"
git push --set-upstream origin develop

git checkout master
git merge develop
git push

4. git checkout develop
nano main.py
вносим изменения

git add .
git commit -m "Добавил время"
git push

git checkout master
nano main.py
вносим изменения
git add .
git commit -m "Добавил время и еще вывод"
git push

git merge develop
Далее разрешаем конфликт, удаляем >>> === <<<

 git add . 
 git commit -m "Разрешил конфликт слияния между master и develop"
 git push


5. Делаем еще несколько коммитов

git log --oneline
218dd64 (HEAD -> master, origin/master) Свежая фича
4a49b21 Добавил фичу
ef8ee61 Конфликт
dcb518e Добавил время и еще вывод
4b1c25c (origin/develop, develop) Добавил время
0b0dfc2 Добавлены изменение какие-то
75d30b1 initial commit

вернемся к прошлому коммиту
git revert 218dd64 --no-edit

потом делаем пулл 
git pull --no-rebase

git push

6. git tag -a v1.0.0 -m "Версия 1.0.0 - первый стабильный релиз"
git push origin v1.0.0

7.


