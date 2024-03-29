---
## Front matter
title: "ОТЧЕТ 
ПО ЛАБОРАТОРНОЙ РАБОТЕ №1"
subtitle: "дисциплина: Архитектура компьютера"
author: "Шурыгин Илья Максимович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью моей работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Необходимо установить виртуальную машину и проверить, работают ли программы.

# Выполнение лабораторной работы

1. Запускаем терминал и переходим в каталог /var/tmp. Создаем каталог с нашим именем или проверяем его наличие с помощью команды ls. Запускаем виртуальную машину VirtualBox &. Также меняем комбинацию для хост- клавиши, которая используется для освобождения курсора мыши, который может захватить виртуальная машина.(рис. [-@fig:001])(рис. [-@fig:002])(рис. [-@fig:003])

![Проверяем наличие каталога с помощью команды ls](image/1.png){ #fig:001 width=70% }

![Запуск виртуальной машины](image/2.png){ #fig:002 width=70% }

![Смена хост-клавиши](image/3.png){ #fig:003 width=70% }


2. Создаем папку для виртуальной машины. Затем, выбираем все необходимые параметры: тип операционной системы — Linux, Fedora, размер основной памяти виртуальной машины — от 2048 МБ, конфигурацию жёсткого диска — загрузочный, VDI, динамический виртуальный диск, размер диска — 82 ГБ. Его расположение: /var/tmp/имя_пользователя/fedora.vdi. Доступный объем видеопамяти увеличиваем до 128 МБ. В настройках виртуальной машины во вкладке Носители добавляем новый привод оптических дисков и выбираем образ: /afs/dk.sci.pfu.edu.ru/common/files/iso/Fedora-Live-Desktop-i686-19-1.iso.(рис. [-@fig:004])(рис. [-@fig:005])(рис. [-@fig:006])(рис. [-@fig:007])(рис. [-@fig:008])(рис. [-@fig:009])(рис. [-@fig:013])

![Окно «Имя машины и тип ОС»](image/4.png){ #fig:004 width=70% }

![Окно «Размер основной памяти»](image/5.png){ #fig:005 width=70% }

![Окно определения типа подключения виртуального жёсткого диска](image/6.png){ #fig:006 width=70% }

![Окно определения формата виртуального жёсткого диска](image/13.png){ #fig:013 width=70% }

![Окно определения размера виртуального динамического жёсткого диска и его расположения](image/7.png){ #fig:007 width=70% }

![Настройка виртуальной машины](image/8.png){ #fig:008 width=70% }

![Выбор образа оптического диска](image/9.png){ #fig:009 width=70% }

3. Запускаем виртуальную машину. Затем, устанавливаем систему на жестких диск - Install to Hard Drive. При необходимости корректируем часовой пояс, раскладку клавиатуры.(рис. [-@fig:010])

![Окно запуска установки образа ОС](image/10.png){ #fig:010 width=70% }

4. После подготовительных действий нажимаем: начать установку. При установке: задаем пароль для пользователя root (суперпользователь администратор) и создаем обычного пользователя с вашим логином. После окончания установки, следует закрыть окно установщика и выключить систему. После того, как виртуальная машина отключится, следует изъять образ диска из дисковода, при этом сам дисковод удалять не следует!(рис. [-@fig:011])

![Извлечение образа диска](image/11.png){ #fig:011 width=70% }

# Домашнее задание:

1. Дождался загрузки графического окружения и открыла терминал. В окне терминала проанализировал последовательность загрузки системы, выполнив команду dmesg. Получим версию ядра Linux (Linux version).(рис. [-@fig:014])

![Linux version](image/14.jpg){ #fig:014 width=70% }

2. Получим частоту процессора (Detected Mhz processor).(рис. [-@fig:015])

![Detected Mhz processor](image/15.jpg){ #fig:015 width=70% }

3. Получим модель процессора (CPU0).(рис. [-@fig:016])

![CPU0](image/16.jpg){ #fig:016 width=70% }

4. Получим объем доступной оперативной памяти (Memory available).(рис. [-@fig:017])

![Memory available](image/17.jpg){ #fig:017 width=70% }

5. Получим тип обнаруженного гипервизора (Hypervisor detected) и тип файловой системы корневого раздела. Последовательность монтирования файловых систем.(рис. [-@fig:018])

![Hypervisor detected](image/18.jpg){ #fig:018 width=70% }


# Контрольные вопросы:

1. Информация, которую содержит учётная запись пользователя:

- Имя пользователя (user name) - в рамках системы имя должно быть уникальным. В именах должны использоваться только английские буквы, числа и символы _ и . (точка)

- Идентификационный номер пользователя (UID) - является уникальным идентификатором пользователя в системе. Система отслеживает пользователей по UID, а не по именам.

- Идентификационный номер группы (GID) - обозначает группу, к которой относится пользователь. Каждый пользователь может принадлежать одной или нескольким группам. Принадлежность пользователя к группе устанавливает системный администратор, чтобы иметь возможность ограничивать доступ пользователей к тем или иным ресурсам системы.

- Пароль (password) - пароль пользователя в зашифрованном виде.

- Полное имя (full name) - помимо системного имени может присутствовать полное имя пользователя, например фамилия и имя.

- Домашний каталог (home directory) - каталог, в который попадает пользователь после входа в систему. Подобный каталог имеется у каждого пользователя, все пользовательские каталоги хранятся в директории /home.

- Начальная оболочка (login shell) - командная оболочка, которая будет запускаться при входе в систему. Например, /bin/bash.

2. Команды терминала:

«команда> - help - для получения справки по команде
cd - для перемещения по файловой системе
Is - для просмотра содержимого каталога
du <имя-директории» - для определения объёма каталога
mkdir/irdir(rm -r) - для создания / удаления каталогов
touch/rm - для создания / удаления файлов
chmod - для задания определённых прав на файл / каталог
history - для просмотра истории команд

3. Файловая система - порядок, определяющий способ организации, хранения и именования данных на носителях информации в компьютерах, а также в другом электронном оборудовании: цифровых фотоаппаратах, мобильных телефонах и т. п. Файловая система определяет формат содержимого и способ физического хранения информации, которую принято группировать в виде файлов. Конкретная файловая система определяет размер имен файлов и (каталогов), максимальный возможный размер файла и раздела, набор атрибутов файла. Некоторые файловые системы предоставляют сервисные возможности, например, разграничение доступа или шифрование файлов.

4. df - утилита, показывающая список всех файловых систем по именам устройств, сообщает их размер, занятое и свободное пространство и точки монтирования. При выполнении без аргументов команда mount выведет все подключенные в данный момент файловые системы.

5. Удалить зависший процесс можно с помощью команды killall - killall «название зависшего процесса>

# Выводы

Вывод: я приобрел практические навыки по установке операционной системы Linux на виртуальную машину, запустил терминал и с его помощью установил pandoc, texlive.