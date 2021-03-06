# Инструкция по работе в Git

![Поехали!!!](3qtr.jpg)

## Введение

 Перед тем как начинать работать над контролем версий файлов в git, нужно создать папку на жестком диске или другом носителе.

Далее эту папку открыть в Visual studio code, затем с помощью команд terminala проверяем установлен ли git на компьютере и какая версия. Для этого используем команду:

    git --version

Если на консоли отобразилась версия git, то продолжаем работать согласно инструкции, если нет устанавливаем git на компьютер.

Затем прописываем свои данные с помощью команд:

    git config --global user.name
    git config --global user.email

# Создание файла в репозитарии и его сохранение

Перед тем как создать папку с репозитарием проверяем статус с помощи команды:

    git status

Создаем локальный репозитарий в которой сейчас находится наша папка:

    git init

В данном репозитарии создаем файл и начинаем с ним работать.

Для того чтобы сохранить изменения в текущей версии файла, нужно сначало сохранить на диск (CTR+S), далее фиксируем его в репозитарии:

    git add name_file

После сохраняем текущее состояние версии и добовляем коментарии с помощью:

    git commit -m "Текущие коментарии"

Также можно сделать git commit без комады git add для этого надо ввести:

    git commit -a

## Основные команды при работе в Git

Отображение журнала всех сохраненных версий осуществляется с помощью команды:

    git log  -  полная версия
    git log --oneline  -  короткая версия
    git log --all  -  вся история 
    git log --graph - графическая версия

также можно сочетать все перечисленные комбинации, например:

    git log --oneline --all --graph

Для того чтобы отобразить разницу между состояниями текущим и сохраненным, используют следующее:

    git diff

Чтобы перейти в нужную версию применяют команду:

    git checkout
    для этого берут первых 4 символа кода версии, например:
    git checkout ba28
    git checkout master  -  позволяет перейти в        
                            последнюю версию основной ветки

## Отображение и создание в Git новых веток файла

Отображение веток производится с помощь команды:

    git branch

Чтобы добавить новую ветку необходимо ввести команду:

    git branch <имя_ветки>

Для удаления ненужной ветки, которая уже влилась в другую версию используют команду:

    git branch -d <имя_ветки>


## Сливание веток

 для слияния веток используют команду:

    git merge <имя_ветки>

Для того чтобы слить (объединить) две ветки в одну нужно находится в той ветке в которую мы хотим поместить выбранную для слияния ветку, например если мы хотим, чтобы из ветки branch_name все попало в ветку master, то нам нужно сделать следующее:

    git checkout master
    git merge branch_name
    
После слияния веток ненужные ветки надо удалить

## Синтаксис языка MarkDown

Для большего разнообразия и осознания написанного текста можно использовать элементы синтаксиса, такие как:

    Заголовки - для это перед текстом ставим "#"
    например:

# Заголовок первого уровня
## Заголовок второго уровня


    Списки - чтобы списки были ненумерованными нужно перед строкой через "пробел" написать "*" или "+"

* Первая строка

+ Вторая строка

    Списки с нумерацией - чтобы списки были нумерованными нужно перед строкой через "пробел" написать "1."

    1. Номер один
    2. Номер два


    Выделение текста - если требуется текст сделать полужирным, то его нужно обрамить с двух сторон вот так "**", например:

**Жирный текст**

    для выделения текста курсивом, его нужно обрамить с двух сторон "*", например:

*Текст курсивом*

    И для того чтобы текст был другого цвета его также нужно обрамить с двух сторон "~", например:

`Цветной текст`

## "Горячие" клавиши и не только

Для того чтобы работа в git была более быстрой, продуктивной и менее затратной, в данной програмее можно использовать "горячии"  клавиши, такие как:

* стрелки вверх и вниз - выбор ранее введеных команд;

* TAB - при начале набора текста довводит текст в терминале, если этот текст ранее вводился;

+ Q - выход из режимов;

+ clear - короткая команда, с помощью которой можно очистить содержимое терминала.

# **`КОНЕЦ`**

## *До скорой встречи!*

![милый дом](Home.jpg)

P.S. Для того чтобы картинки не высвечивались на терминале их нужно добавить в файл .gitignore

Правка из GitHub
