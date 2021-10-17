# evernote-example
Скрипт для работы с сервисом Evernote [Evernote](https://evernote.com).
Evernote - это система организации информации.
Дя работы вам потребуется зарегистрироваться на сайте и запросить API Key.

## Окружение

Полученные после регистрации персональные данные присвоить переменным окружения в файле ".env":
```python
    EVERNOTE_CONSUMER_KEY = Ваш EVERNOTE_CONSUMER_KEY
    EVERNOTE_CONSUMER_SECRET = Ваш EVERNOTE_CONSUMER_SECRET
    EVERNOTE_PERSONAL_TOKEN - Ваш EVERNOTE_PERSONAL_TOKEN

    JOURNAL_TEMPLATE_NOTE_GUID = ?
    JOURNAL_NOTEBOOK_GUID = ?

    INBOX_NOTEBOOK_GUID = ?
```
Python3 должен быть уже установлен.

## Зависимости
Используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:
```python
pip install -r requirements.txt
```

## Запуск
1) add_note2journal.py - скрипт для добавления записей в журнал:
    - получает пользователя Evernote и его записи
    - добавляет новую запись
    - для запуска нужно указать дату в качестве аргумента:
   ```python
   python add_note2journal.py 'YYYY-MM-DD'
   ```
2) list_notebooks.py - скрипт для вывода списка записей:
    - получает пользователя Evernote
    - выводит список его записей
    - запускается командой 
    ```python
    python3 list_notebooks.py
    ```
3) dump_inbox.py - скрипт для вывода текста записей:
    - получает пользователя Evernote
    - выводит текст его записей по заданному параметру (количество записей)
    - для запуска нужно указать количество записей в качестве аргумента:
   ```python
   python dump_inbox.py 'количество записей'
   ```

## Цель проекта
Код написан в образовательных целях на онлайн-курсе для веб-разработчиков https://dvmn.org
