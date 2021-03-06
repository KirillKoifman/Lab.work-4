# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ

### Факультет физико-математических и естественных наук
 Кафедра прикладной информатики и теории вероятностей
 ====================================================


ОТЧЕТ
ПО ЛАБОРАТОРНОЙ РАБОТЕ №4
===============


дисциплина:  Операционные системы 



Студент: Койфман Кирилл Дмитриевич

Группа: НПИбд-01-21






## Введение
___
## Цель работы.
Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.
## Задачи.
1. Определить полное имя вашего домашнего каталога. Далее относительно этого каталога будут выполняться последующие упражнения.
2. Выполнить следующие действия:

2.1. Перейти в каталог /tmp.

2.2. Вывести на экран содержимое каталога /tmp. Для этого использовать команду ls
с различными опциями. Пояснить разницу в выводимой на экран информации.

2.3. Определить, есть ли в каталоге /var/spool подкаталог с именем cron?

2.4. Перейти в домашний каталог и выведите на экран его содержимое. Определить, кто является владельцем файлов и подкаталогов?

3. Выполнить следующие действия:

3.1. В домашнем каталоге создать новый каталог с именем newdir.

3.2. В каталоге ~/newdir создать новый каталог с именем morefun.

3.3. В домашнем каталоге создать одной командой три новых каталога с именами
letters, memos, misk. Затем удалить эти каталоги одной командой.

3.4. Попробовать удалить ранее созданный каталог ~/newdir командой rm. Проверить,
был ли каталог удалён.

3.5. Удалить каталог ~/newdir/morefun из домашнего каталога. Проверить, был ли
каталог удалён.

4. С помощью команды man определить, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов,
входящих в него.

5. С помощью команды man определить набор опций команды ls, позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога
с развёрнутым описанием файлов.

6. Использовать команду man для просмотра описания следующих команд: cd, pwd, mkdir,rmdir, rm. Пояснить основные опции этих команд.

7. Использовать информацию, полученную при помощи команды history, выполнить модификацию и исполнение нескольких команд из буфера команд.
## Ход работы.
---
### 1 задание.
Определим полное имя домашнего каталога:

Перейдём в домашний каталог:

```
cd
```
>Команда cd предназначена для перемещения по файловой системе. Для перехода в домашний каталог пользователя следует использовать команду cd без
параметров или cd ~.

Выведем полное имя домашнего каталога:
```
pwd
```
>Команда pwd позволяет определить абсолютный путь к текущему каталогу, а также получить абсолютное имя текущего каталога пользователя.

И мы получаем результат:

![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/1.png)
:--:
*Результат выполнения команды pwd*
### 2 задание.
#### 2.1 задание.
Перейдём в каталог /tmp и выведем его содержимое:

Перейдём в каталог /tmp с помощью команды cd:
```
cd /tmp
```
#### 2.2 задание.
Выведем на экран содержимое каталога /tmp, используя команду ls с несколькими уникальными опциями:
```
ls
```
>Команда ls используется для просмотра содержимого каталога.


![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-1.png)
:--:
*Использование команды ls без каких-либо опций*
 
 Проверим работу команды ls в комбинации с разными опциями:
 
 ```
 ls -l
 ```
 >При использовании опции -l выведется дополнительная информация о каждом файле данного каталога
 
 ![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-5.png)
  :--:
*Использование команды ls в сочетании с опцией -l*

 ```
 ls -a
 ```
 >При использовании опции -a выведется весь список файлов, включая скрытые
 
 ![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-2.png)
 :--:
*Использование команды ls в сочетании с опцией -a*
 ```
 ls -R
 ```
 >При использовании опции -R будет произведён рекурсивный вывод списка всех файлов и подкаталогов
 
 ![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-4.png)
 :--:
*Использование команды ls в сочетании с опцией -R*
#### 2.3 задание.
Определим, есть ли в каталоге /var/spool подкаталог cron:

Вернёмся в домашний каталог и перейдём в каталог /spool, указав путь к нему:
```
cd
cd /var/spool
```
Теперь выведем содержимое данного каталога:
```
ls
```
 ![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-6.jpeg)
 :--:
*Вывод содержимого каталога /spool*
#### 2.4 задание.
Перейдём в домашний каталог, выведем на экран его содержимое, а также определим, кто является владельцем файлов и подкаталогов:
```
cd
ls
```
 ![Картинка](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-7.png)
 :--:
*Вывод содержимого домашнего каталога(каталог cron отсутствует в нём) *
```
ls -l
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/2.2-8.png)
:--:
*Вывод информации о владельце файлов и подкаталогов домашнего каталога*
### 3 задание.
#### 3.1 задание.
Создадим в домашнем каталоге подкаталог newdir:
```
mkdir newdir
```
>Команда mkdir используется для создания каталогов.

![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/3.1.png)
:--:
*Создание подкаталога newdir и проверка на успешность выполнения этой команды с помощью команды ls(каталог был создан)*
#### 3.2 задание.
Создадим в каталог morefun в каталоге newdir:
```
mkdir morefun
```

![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/3.2.png)
:--:
*Создание подкаталога morefun и проверка на успешность выполнения этой команды с помощью команды ls(каталог был создан)*
#### 3.3 задание.
Создадим в домашнем каталоге одной командой 3 новых каталога с именами letters, memos, misk:

Вернёмся в домашний каталог:
```
cd 
```
Создание каталогов letters,memos и misk:
```
mkdir letters memos misk
ls
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/3.3-1.png)
:--:
*Использование команды mkdir для создания 3-х каталогов(каталоги были созданы)*

Теперь удалим ранее созданные каталоги с помощью команды rm:
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/3.3-2.png)
:--:
*Удаление 3-х ранее созданных каталогов и проверка на корректность выполнения команды rm при помощи команды ls*
>Команда rm используется для удаления файлов и/или каталогов.
>>опция -r предназначена для произведения рекурсивного удаления(перед удалением пользователь получает запрос на подтверждение об удалении)
#### 3.4 задание.
Попробуем удалить ранее созданный каталог newdir командой rm:
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/3.4.png)
:--:
*Неудачная попытка удалить каталог newdir*
#### 3.5 задание.
Удалим ранее созданный каталог morefun командой rm:
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/3.5.png)
:--:
*Удаление каталога morefun и проверка командой ls(каталог был удалён)*
### 4 задание.
С помощью команды man определим, какую опцию команды ls нужно использовать для просмотра содержимого как указанного каталога, так и его подкаталогов:
```
man ls
```
>Команда man используется для просмотра (оперативная помощь) в диалоговом режиме руководства (manual) по основным командам операционной системы
типа Linux.

![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/4.1.png)
:--:
*Использование команды man*
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/4.2.png)
:--:
*Содержимое руководства(manual)*

Просмотрев руководство по команде ls, можно сказать, что опцией для просмотра содержимого как указанного каталога, так и его подкаталогов, является опция -R.
### 5 задание.
С помощью команды man определим, какой набор опций команды ls нужно использовать для сортировки по времени последнего изменения выводимый список содержимого каталога с развёрнутым описанием:
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/4.1.png)
:--:
*Использование команды man*
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/4.2.png)
:--:
*Содержимое руководства(manual)*

Просмотрев руководство по команде ls, можно сказать, что набором опций для сортировки по времени последнего изменения выводимый список содержимого каталога с развёрнутым описанием, является набор из опций -l и -t.
>Опция -l позволяет выводить развёрнутое описание каждого файла

>Опция -t позволяет  отсортировать файлы и каталоги по времени последнего изменения
### 6 задание.
Используем команду man для просмотра описания команд cd, pwd, mkdir, rmdir, rm:

```
man cd
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/6.1-2.png)
:--:
*Руководство по команде cd*

>Опция -L отвечает за возможность перехода по символическим ссылкам

>Опция -P позволяет разыменовывать символические ссылки

```
man pwd
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/6.2-2.png)
:--:
*Руководство по команде pwd*
>Опция -L позволяет избежать процесса разыменования символических ссылок

>Опция -P преобразовывает символические ссылки в исходные данные
```
man mkdir
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/6.3-2.png)
:--:
*Руководство по команде mkdir*
>Опция -m устанавливает права доступа для создаваемой директории

>Опция -p позволяет создать все директории, указанные внутри пути
```
man rmdir
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/6.4-2.png)
:--:
*Руководство по команде rmdir*
>Опция -P удаляет указанную папку и её родительские каталоги

>Опция -v выводит диагностический текст для каждого обработанного каталога
```
man rm
```
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/6.5-2.png)
:--:
*Руководство по команде rm*
>Опция -r или -R производят рекурсивное удаление

>Опция -i перед удалением каталога отправляет пользователю запрос на подтверждение команды 
>Опция -f выполняет принудительное удаление файлов и каталогов

### 7 задание.
Используем команду history для вывода всех ранее выполненных команд и модифицируем одну из них:
```
history
```
>Для вывода на экран списка ранее выполненных команд используется команда history.
![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/7.3.jpeg)
:--:
*История выполненных в командной строке команд*

Модифицируем команду под номером 240:

>Конструкция для модификации команды выглядит так:  
!<номер_команды>:s/<что_меняем>/<на_что_меняем>

![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/7.4.jpeg)
:--:
*Использование специальной инструкции для модификации команды №240*

![Picture](https://raw.githubusercontent.com/KirillKoifman/Lab.work-4/main/LAB_4/7.2.jpeg)
:--:
*Использованной модифицированной команды ls под №240*

## Вывод
Вследствие проделанной работы, можно сказать, что мной были изучены и приобретены основные навыки взаимодействия с системой посредством командной строки. 

### Ответы на контрольные вопросы.
1. Командная строка - это программное средство для выполнения пользовательского ввода команд и инструкций и получения соответствующих результатов. 
2. При помощи команды pwd. Например, для получения абсолютного пути 
3. Определить только тип файлов и их имена в текущем каталоге можно с помощью команды ls с опцией -l.
4. Отобразить информацию о скрытых файлах можно с помощью команды ls -a.
5. При помощи команд rm или rmdir можно удалить файл и каталог?       Cделать это одной и той же командой воможно.
6. Вывести информацию о последних выполненных пользователем командах можно с помощью команды history.
7. Чтобы воспользоваться историей команд для их модифицированного выполнения необходимо ввести в командную строку команду history, затем выбрать желаемую команду для модификации и использовать следующую конструкцию: 
!<номер_команды>:s/<что_меняем>/<на_что_меняем>
8. Команда mkdir, который используется для создания сразу 3-х каталогов: mkdir dir1 dir2 dir3.
9. Символ экранирования - это символ \, который позволяет использовать управляющие символы без их интерпретации командной оболочкой.
10. При использовании опции -l с командой ls выводится дополнительная информация о каждом файле каталога.
11. Относительный путь к файлу - это путь к файлу, строящийся относительно каталога, в котором пользователь находится в данный момент.
12. Чтобы получить информацию о какой-либо вас команде, нужно использовать команду man.
13. Клавиша Tab служит для автоматического дополнения
вводимых команд.
