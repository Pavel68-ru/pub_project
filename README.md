# Практикум Яндекс по GIT


**GIT** - это система контроля версий, которая помогает отслеживать изменения в проекте. Этот инструмент можно использовать как для индивидуальной, так и для командной работы.

Скачать и установить GIT можно с официального сайта [GIT_Windows](https://git-scm.com/download/win).  

Перечень команд GIT  



```bash 
git init - создание папки репозитория  
git status - вывод состояния репозитория  
git status --ignored - вывод состояния игнориемуых файлов
git add --all - добавление отслеживания всех файлов  
git add . - добавление отслеживания всех файлов  
git commit -m "<комментарий>" - добавить коммит с коментарием
git commit --amend - изменение последнего коммита (HEAD)
git commit --amend --no edit - изменение последнего коммита (HEAD) без изменения комментария
git commit --amend -m "<комментарий>" - изменение последнего коммита (HEAD) c изменением комментария
git clone <url> - клонирование удаленного репозитория
git log - вывод истории изменений
git log --oneline - сокращенный вывод истории (хеш, комментарий)
git remote add <имя репозитория> <репозиторий GitHub> - добавление внешнего репозитория  
git remote -v - информация об удаленном репозитории  
git push - отправка изменений на удаленный репозиторий
git diff - показывает разницу, без параметров между последним коммитом и измененным файлом в статусе modified
git diff --staget - показывает разницу проиндексированных файлов, относительно предыдущих
git diff <hashA> <hashB> - показывает разничу между версии файлов
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


### Сравнение версий файлов

git diff - позваляет посмотреть измененные файлы.
git diff <hashA> <hashB> - позволяет сравнить отслеживаемы изменения, при расположении <hashB> <hashA> можно посмотреть обратную историю.  
Знак минус (-) и текст красного цвет обозначет, что данные были удалены.  
Знак плюс (+) и текс зеленого цвета обозначает, что данные были добавлены.  


----

### Игнорирование файлов в Git

Для игнорирования файлов в каталоге отслеживания git, необходимо создать файл **.gitignore** и записать в него название игнорируемых файлов.  
В файл **.gitignore** можно добавлять комментарии, перечень файлов по одному на строку или логические выражения типа doсs/**/tmp.

```bash
# игнорировать все файлы в каталоге build
build/

# игнорировать все .log файлы
*.log

# не игнорировать *.log файлы в examples
# потому что это пример для документации
!examples/**/*.log 
```

Материалы [Яндекс практикум](https://practicum.yandex.ru/profile/git-basics/)  
 


