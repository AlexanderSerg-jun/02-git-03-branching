## Домашнее задание к занятию «Ветвления в Git»
# Задание «Ветвление, merge и rebase»
# Решение 
# Шаг 1. Создал каталог branching и файлы merge.sh и rebase.sh с содержимым:
![Создание каталога](/img/image.png)
![Создание файлов](/img/image-1.png)
# Шаг 2. Создал коммит с описанием prepare for merge and rebase и отправим его в ветку main:
![commit and push](/img/image-2.png)
## Подготовка файла merge.sh
# Шаг 1. Создаем ветку git-merge:
![Создание ветки](/img/image-3.png)

# Шаг 2. Заменим содержимое файла merge.sh на указанный в задании скрипт:
![Новое содержимое файла](/img/image-4.png)
# Шаг 3. Создаем коммит merge: @ instead *, отправляем изменения в репозиторий.
![Создание коммита и отправка в репозиторий](/img/image-5.png)

# Шаг 4. Вносим изменения в файл merge.sh.
![Изменения в файле](/img/image-6.png)
# Шаг 5. Создаем коммит merge: use shift и отправляем изменения в репозиторий
![Новый коммит и отправка в репозиторий](/img/image-7.png)

## Изменим main
# Шаг 1. Вернемся в ветку main
![Возврат в ветку main](/img/image-8.png)
# Шаг 2. Изменим файл rebase.sh
![Изменения в файле](/img/image-9.png)
# Шаг 3. Отправляем изменения в ветку main:
![Отправка изменений](/img/image-10.png)

## Подготовка файла rebase.sh
# Шаг 1. С помощью команды git log находим хеш коммита prepare for merge and rebase и выполняем git checkout на него:
![Хэш](/img/image-11.png)
![Checkout](/img/image-12.png)
# Шаг 2. Создадим ветку git-rebase, основываясь на текущем коммите:
![Новая ветка](/img/image-13.png)
# Шаг 3. Изменим содержимое файла rebase.sh.
![Новое содержимое](/img/image-14.png)
# Шаг 4. Отправим эти изменения в ветку git-rebase с комментарием git-rebase 1:
![Отправка изменений](/img/image-15.png)
# Шаг 5. Сделалаем ещё один коммит git-rebase 2 с пушем, заменив echo "Parameter: $param" на echo "Next parameter: $param":
![Новое содержимое](image-16.png)
![Коммит и пуш](/img/image-17.png)


## Промежуточный итог
# Проверим, что у меня получилось на network странице по ссылке https://github.com/AlexanderSerg-jun/02-git-03-branching/network
![Промежуточный итог](/img/image-18.png)

## Merge
# Переключаемся на ветку main. Сливаем ветку git-merge в main и отправляем изменения в репозиторий:
![chekcout](/img/image-20.png)
![merge](/img/image-21.png)
![push](/img/image-19.png)

## Rebase
# Шаг 1. и Шаг 2. Выполнил rebase ветки git-rebase на main, создав конфликт:

![conflict](/img/image-22.png)
# Смотрим содержимое файла rebase.sh
![rebase](/img/image-23.png)
# Шаг 3. Удаляю метки, выбираю вариант echo "$@ Parameter #$count = $param"

# Шаг 4. Сообщаю Git, что конфликт решён и продолжаю rebase
# Шаг 5. Опять получаю конфликт:
![New conflict](/img/image-24.png)
Редактирую файл rebase.sh, оставляю строчку echo "Next parameter: $param".
# Шаг 6. Продолжаем rebase. Открывается текстовый редактор, предлагающий написать комментарий к новому объединённому коммиту
![alt text](/img/image-25.png)
# Шаг 7. Пытаемся выполнить пуш и видим, что команда завершается с ошибкой:
![ОШибка](/img/image-26.png)
# Шаг 8. Пытаюсь выполнить пуш с флагом force и это удается сделать:
![Пуш с флагом force](/img/image-27.png)
# Шаг 9 .  Теперь можно смержить ветку git-rebase в main без конфликтов и без дополнительного мерж-комита простой перемоткой:
![](/img/image-28.png)
Ссылка на итоговый network график: https://github.com/AlexanderSerg-jun/02-git-03-branching/network