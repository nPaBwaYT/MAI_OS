# MAI_OS

Репозиторий лабораторных работ группы М8О-213Б-23 по дисциплине «Операционные системы»

## Ссылки

[Варианты ЛР и прогресс](https://docs.google.com/spreadsheets/d/1mJrtBqrRkpXkm1YgtC6Uc45YuXXP_kXlPPegMOU72J8/edit?usp=sharing)

[Запись в очередь на очную защиту](https://docs.google.com/spreadsheets/d/1WCOanvdveBgt0ekh2jVxqXzK_pkz9U3Lxf8ym2S16Sg/edit?usp=sharing)

## Порядок сдачи

Каждая лабораторная работа сдается в 2 этапа: код-ревью и очная 
защита. Чтобы допуститься к очной защите, необходимо пройти код-ревью. Без 
прохождения обоих этапов лабораторная работа не может быть сданной (даже на 
оценку 3).

### Код-ревью

Необходимо прикрепить написанный код и отчет в pull request к этому репозиторию. 
Название pull request'а должно соответствовать правилам наименования. Все 
изменения должны быть только в папке лабораторной работы. Каждая лабораторная 
работа сдается в отдельном pull request'е.

### Очная защита

После прохождения этапа код-ревью необходимо записаться в очередь на очную 
защиту работы и прийти к соответствующему времени.

Этапы очной защиты:

* Демонстрация работы программы
* Вопросы по работе программы
* Вопросы по теории
* Вопросы по системным вызовам

## Требования

### Лабораторная работа №1

Правила оформления кода:

* Код должен быть написан на C или C++
* Операционная система: Linux, MacOS или Windows
* Обязательно используются системные вызовы
* Все, что относится к стандартной библиотеке C++, кроме `std::string` и 
`std::vector`, запрещено
* `stdio.h`, `threads.h`, `stdatomic.h` из стандартной библиотеки C запрещены
* Весь исходный код находится в папке `src`
* Бинарных файлов вроде `a.out`, `main.o` быть не должно
* Папок вроде `.vscode`, `.idea` быть не должно
* На каждый системный вызов должна быть организована проверка на ошибку
* Код должен быть легко читаем (правильно расставлены отступы, переменные и 
функции имеют осмысленные названия)

Правила оформления отчета:

* Отчет должен быть в формате PDF, редактировать можно в любом формате 
(Word, Latex и тд)
* Отчет должен находиться в папке `doc`
* Отчет должен содержать вывод утилиты `strace` для Linux, `dtrace` для MacOS 
или `nttrace` для Windows. Должны быть выделены системные вызовы, которые были 
вызваны из пользовательского кода
* Структура отчета должна соответствовать [примеру](https://docs.google.com/document/d/13ydQ0_xVeFhwN5AY242K4Sf8GtPr2wt3/edit)

### Лабораторная работа №2

Правила оформления кода:

* Код должен быть написан на C или C++
* Операционная система: Linux, MacOS или Windows
* Обязательно используются системные вызовы
* Все, что относится к стандартной библиотеке C++, кроме `std::string` и 
`std::vector`, запрещено
* `stdio.h`, `threads.h`, `stdatomic.h` из стандартной библиотеки C запрещены
* Решение на атомиках приветствуется, но только когда есть выполненная работа без них
* Весь исходный код находится в папке `src`
* Бинарных файлов вроде `a.out`, `main.o` быть не должно
* Папок вроде `.vscode`, `.idea` быть не должно
* На каждый системный вызов должна быть организована проверка на ошибку
* Код должен быть легко читаем (правильно расставлены отступы, переменные и 
функции имеют осмысленные названия)
* Рекомендуется включать санитайзер потоков -fsanitize=thread во флаги 
компиляции для компиляторов GCC и Clang для Linux/macOS

Правила оформления отчета:

* Отчет должен быть в формате PDF, редактировать можно в любом формате 
(Word, Latex и тд)
* Отчет должен находиться в папке `doc`
* Отчет должен содержать вывод утилиты `strace` для Linux, `dtrace` для MacOS 
или `nttrace` для Windows. Должны быть выделены системные вызовы, которые были 
вызваны из пользовательского кода
* Структура отчета должна соответствовать [примеру](https://docs.google.com/document/d/13ydQ0_xVeFhwN5AY242K4Sf8GtPr2wt3/edit)
* Должна присутствовать таблица, иллюстрирующая коэфициент прироста 
производительности при использовании K потоков по сравенению с однопоточным 
решением. Берём любые 5 чисел K. Одно из K должно быть равно числу логических 
ядер на компьютере, где решение было протестировано

## Дедлайны

* на оценку 5 – не позднее 2 недель со дня выдачи
* на оценку 4 – не позднее 3 недель со дня выдачи
* на оценку 3 – позднее 3 недель со дня выдачи

В эти сроки должны быть пройдены и код-ревью, и очная сдача. Если код-ревью 
пройдено не позднее 2 недель со дня выдачи, а очная сдача пройдена позднее 2 
недель и не позднее 3 недель со дня выдачи, будет выставлена оценка 4.  

## Инструкция к Pull Request

Для лабораторных работ, начиная со второй, начинаем с пункта 4

1) Делаем Fork этого репозитория. Для этого в правом верхнем углу есть кнопка
`Fork`

2) Клонируем репозиторий на свое устройство и переходим в него

```
git clone https://github.com/$GITHUB_USERNAME/MAI_OS
```

3) Переходим в него

```
cd MAI_OS
```

4) Меняем текущую ветку на `main`

```
git checkout main
```

5) Создаем новую ветку согласно правилам наименования.

```
git checkout -b $BRANCH_NAME
```

6) Делаем задание лабораторной работы в соответствующей директории 🙂

7) Коммитим внесенные изменения

```
git commit -a --message='$COMMIT_MESSAGE'
```

8) Загружаем коммиты на Github

```
git push --set-upstream origin $BRANCH_NAME
```

9) Открываем ваш репозиторий на Github, жмем `Create pull request`. Pull Request 
делаем в этот репозиторий (papey08/MAI_OS)


### Правила наименования

Формат названия ветки: <Фамилия>-lab<Номер ЛР из 2 цифр>

*Например: Ivanov-lab01, Petrov-lab02*

Формат названия Pull Request: <Фамилия Имя> <Группа полностью> lab<Номер ЛР из 2 цифр>

*Например: Иванов Иван М8О-213Б-23 lab01*

Формат названия директории: lab<Номер ЛР из 2 цифр>

*Например: lab01, lab02*
