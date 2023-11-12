# Практикум Яндекс по GIT


**GIT** - это система контроля версий, которая помогает отслеживать изменения в проекте. Этот инструмент можно использовать как для индивидуальной, так и для командной работы.

Скачать и установить GIT можно с официального сайта [GIT_Windows](https://git-scm.com/download/win).  

Перечень команд GIT  



```bash 
git init - создание папки репозитория  
git status - вывод состояния репозитория  
git add --all - добавление отслеживания всех файлов  
git add . - добавление отслеживания всех файлов  
git commit -m "<комментарий>" - добавить коммит с коментарием
git commit --amend - изменение последнего коммита (HEAD)
git commit --amend --no edit - изменение последнего коммита (HEAD) без изменения комментария
git commit --amend -m "<комментарий>" - изменение последнего коммита (HEAD) c изменением комментария
git log - вывод истории изменений
git log --oneline - сокращенный вывод истории (хеш, комментарий)
git remote add <имя репозитория> <репозиторий GitHub> - добавление внешнего репозитория  
git remote -v - информация об удаленном репозитории  
git push - отправка изменений на удаленный репозиторий
```

----


### Подключение удаленного репозитория  


Для подключения удаленного репозитория необходимо:  
Создать на GitHub репозиторий  
Скопировать его SSH URL  
Настроить подключение Git с GitHub  
Открыть локальный каталог с проектом git
Ввсести: *git remote add <имя репозитория> <репозиторий GitHub>*  
Проверить доступность: *git remote -v*  
Провести отправку данных на репозиторий: *git push -u <имя репозитория> master/main*  
Посмотреть вывод и историю  


----


### Статус файлов GIT


**untracked** - *неотслеживаемый*, новый файл в каталоге, GIT видит, но не отслеживает.  

**staged** - *подготовленный*, файл в каталоге подготовленный через команду ***git add <имя файла>***  

**tracked** - *отслеживаемый*, файл в каталоге который подготовлен и закомментирован, противоположность **untracked**  

**modified** - *измененный*, файл в каталоге изменен, необходимо подготовить и закомментировать  


----


### Восстановление  


* GIT позволяет произветси откат изменений на нужную версию с помощью команды:  
```Bash
git reset --hard <commite hash>
```

* GIT позволяет изменить статус файла в каталоге:  
```Bash
git restore --staged <имя файла>
```
Перевод файла из статуса **tracked** в **untracked**.  

* GIT позволяет восстановить измененный файл на состояние до изменения:  
```Bash
git restore <имя файла>
```
Откат изменений  

* Сравнение версий  
```Bash
git вшаа <commite hash> <commite hash>

```

----


### HEAD


**HEAD** - файл в каталоге .git в котором ссылка на последний комментарий *синоним хеша последнего комментария*.  



----


Материалы [Яндекс практикум](https://practicum.yandex.ru/profile/git-basics/)  
 


