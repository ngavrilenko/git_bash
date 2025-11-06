# Работа с git и bash
Выполнила базовые команды, работая с терминалом в Visual Studio Code. Поработала над созданием, перемещением, редактированием и удалением файлов.
Задача 1:
Задание	Выполненная команда
Создать домашнюю директорию через терминал	$ mkdir homedir
Открыть домашнюю директорию через терминал	$ cd homedir
Определить имя папки, в которой вы находитесь	$ pwd
Создать внутри этой папки каталог с именем test1	$ mkdir test1
Перейти в папку test1	$ cd test1
Создать файл 1,2 и 3 внутри каталога test1	$ touch file1.txt file2.txt file3.txt
Проверить содержимое каталога test1	$ ls
file1.txt file2.txt file3.txt
Перейти в домашнюю директорию	$ cd ..
Создать папку test2 внутри домашней директории	$ mkdir test2
Удалить папку test2	$ rmdir test2
Удалить файл 2 из папки test1	$ rm test1/file2.txt
Создать папку в домашней директории test3 и добавить в нее два файла	$ mkdir test3 && touch $_/file4.txt $_/file5.txt
Удалить папку test3	$ rm -r test3
Создать папку test4 в домашней директории	$ mkdir test4
Переместить файлы 1 и 3 из папки test1 в папку test4	$ mv test1/file1.txt test1/file3.txt test4/
Добавить в файл 1 три строки со словами line	$ echo -e "line\nline\nline" >> test4/file1.txt
Посмотреть содержимое файла 1	$ cat test4/file1.txt
Добавьте в файл 3 три строки со словами line	$ echo -e "line\nline\nline" >> test4/file3.txt
Просмотрите содержимое двух файлов (1 и 3) сразу	$ cat test4/file1.txt test4/file3.txt
Используя один из редакторов замените все строки в файле 1	$ nano test4/file1.txt
Задача 2:
Задание	Выполненная команда
Создать домашнюю директорию через терминал	$ mkdir homedir
Зайти в домашнюю директорию через терминал.	$ cd homedir
Создать папку test 3	$ mkdir test3
Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4	$ echo -e "row1\nrow2\nrow3\nrow4" >> test3/file4.txt && echo -e "row1\nrow2\nrow3\nrow4" >> test3/file5.txt && echo -e "row1\nrow2\nrow3\nrow4" >> test3/file6.txt
Найдите строку row2 в файле 5	$ cat test3/file5.txt | grep "row2"
Найдите строку row в папке test3	$ grep -r 'row' test3
Посчитайте сколько строк с содержимым row в файле 6	$ grep -c 'row' test3/file6.txt
Найдите файл 5 внутри папки test3	$ find ./test3 -name "*file5*"
Используя команду find, удалите файл 5	$ find ./test3 -name "*file5*" -delete
Используя команду echo, добавьте слово test в файл 4	$ echo "test" >> test3/file4.txt
Замените слово test в файле 4 на fail	$ sed "s/test/fail/g" test3/file4.txt -i
Добавьте в файл 4 слово test так, чтобы сохранилось содержимое	$ echo "test" >> test3/file4.txt
Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе	$ ps aux
Убейте процесс 666 в консоли	$ kill 666
Узнайте доступность ресурса rusau.net, используя ping	$ ping rusau.net && echo available || echo unavailable
Отправьте 5 пакетов на сайт rusau.net	$ ping -c 5 rusau.net
Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/	$ curl https://petstore.swagger.io/v2/pet/findByStatus?status=available
Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/	$ curl -X POST -H "api_key: special-key" -H "Content-Type: application/json" -d '{"id": 1315, "username": "Iris", "firstName": "Ulyana", "lastName": "Vlasenko", "email": "u-vlasenko@mail.ru", "password": "1234567", "phone": "7654321", "userStatus": 0}'
https://petstore.swagger.io/v2/user
