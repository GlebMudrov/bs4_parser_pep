# Проект парсинга PEP

## Описание проекта
- парсинг данных обо всех документах PEP с сайта https://peps.python.org/.
- сравнение статусов на странице PEP со статусом в общем списке.
- подсчет количества PEP в каждом статусе и общее количество PEP

## Технологии
- Python
- BeautifulSoup
- PrettyTable
- tqdm
- logging

## Запуск проекта

1. Клонировать репозиторий (по SSH)

```
git clone git@github.com:GlebMudrov/bs4_parser_pep.git
```

2. Установить и активировать виртуальное окружение

```
python -m venv venv
. venv/Scripts/activate
```

3. Устанавливаем зависимости проекта

```
pip install -r requirements.txt
```
Примечание: с последний версией pip не все зависимости могут установиться автоматически.
При необходимости недостающие зависимости можно установить вручную:
```
pip install название_библиотеки
```

4. Зайти в директорию проекта src/

```
cd src
```

## Запуск парсеров

<details>
  <summary>Режим "pep"</summary>
  <p>Выводит данные по изменениям в документации PEP</p>
  <code>python main.py pep [параметры]</code>
</details>

<details>
  <summary>Режим "whats-new"</summary>
  <p>Выводит данные по изменениям в языке Python</p>
  <code>python main.py whats-new [параметры]</code>
</details>

<details>
  <summary>Режим "latest-versions"</summary>
  <p>Выводит список версий Python</p>
  <code>python main.py latest-versions [параметры]</code>
</details>

<details>
  <summary>Режим "download"</summary>
  <p>Скачивает документацию Python в zip-архив в папку downloads</p>
  <code>python main.py download [параметры]</code>
</details>

## Параметры парсеров

<details>
  <summary>Режим "-h" или "--help"</summary>
  <p>Выводит справочную информацию о доступных командах программы</p>
  <code>python main.py -h</code>
</details>

<details>
  <summary>Режим "-o" или "--output"</summary>
  <p>Задает способы выводы данных. Возможны следующие варианты:</p>
  <p>1. pretty - выводит данные в виде таблицы в командной строке</p>
  <p>2. file - сохраняет файл в формате .csv в папку results</p>
  <code>python main.py pep -o file</code>
</details>

<details>
  <summary>Режим "-с" или "--clear-cache"</summary>
  <p>Очистка кеша</p>
  <code>python main.py latest-versions -с</code>
</details>

## Автор проекта:  <a href= "https://github.com/GlebMudrov">__Мудров Глеб__<a/>