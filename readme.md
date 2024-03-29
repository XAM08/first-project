# Шпаргалка markdown

## Выделение текста

Вы можете выделять текст в markdown с помощью символов `_` или `*`. Например:

Пример _курсива_ и **жирного** текста.

## Заголовки

Заголовки можно создавать с помощью символа `#`. Чем больше `#`, тем меньше заголовок. Например:

# Заголовок первого уровня
## Заголовок второго уровня
### Заголовок третьего уровня

## Выделение кода

Чтобы выделить текст как код, поместите его в тройные кавычки `````. 

```
mkdir my_project
cd my_project
git init
```
Это лишь некоторые функции markdown. 

## О Хеш
Хеш - уникальный идентификатор для коммита. Используется алгоритм SHA-1

Информация хранится в папке .git


## О логе
Команда git log вызывает полный лог. Такой вызов не всегда удобен когда кол-во коммитов перевалило за тысячи.

Команда git log --oneline позволяет получить сокращенную версию лога


## О HEAD
Файл HEAD находится в папке .git

В нем хранится ссылка на последний коммит

В коммандах git можно передавать HEAD как параметр, он будет восприниматься как хеш последнего коммита


## О статусах файлов
Файлы могут быть в 4 статусах:
1. Untracked
2. Tracked
3. Staged
4. Modified

```mermaid
graph LR;
  Untracked -- "git add" --> Staged;
  Staged    -- "git commit"     --> Tracked;
  Staged    -- "Изменение файла"     --> Modified;
  Modified  -- "git add"     --> Staged;
  Tracked    -- "Изменение файла" --> Staged;

%% стрелка без текста для примера: 
  A --> B;
``` 