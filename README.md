# Курс по языку Python

### Материалы открытого курса [Технопарка](https://park.mail.ru/), осень 2017

#### Установка окружения

Первое, что нужно сделать – поставить последнюю версию Python 3. Ее можно [скачать с официального сайта](https://www.python.org/downloads/).

Чтобы проверить корректность установки нужно запустить команду `python3` в консоли:

```
$ python3
Python 3.5.2 (v3.5.2:4def2a2901a5, Jun 26 2016, 10:47:25)
[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>

```

Должен запуститься интерактивный интерпретатор Python.

Далее необходимо склонировать этот репозиторий в удобное для вас место с помощью `git`:

```
git clone https://github.com/park-python/course.git
cd course
```

Конечно, программа `git` так же [должна быть установлена](https://git-scm.com/downloads).

Нам понадобятся дополнительные Python модули, чтобы не засорять глобальную установку Python, мы
будем работать в виртуальном окружении (virtualenv). Это окружение позволяет устанавливать
питоновские пакеты в локальные директории, тем самым позволяя работать над большим количеством
проектов, использующих разные версии одних и тех же библиотек.

Создадим virtualenv:

```
python3 -m venv env
. env/bin/activate
```

Мы создали и активировали virtualenv. Чтобы его деактивировать нужно выполнить команду `deactivate`:

```
deactivate
```

Но пока деактивировать его не нужно, так как остался последний шаг – установка зависимостей.
Это делается следующей командой:

```
pip install -r requirements.txt
```

`pip` – это менеджер пакетов Python, он автоматически становится доступен после создания и
активации виртуального окружения. В данном случае мы указали ему файл со всеми нашими
зависимостями.

После этого все должно быть готово к просмотру `ipynb` файлов. Перейдите в нужную директорию,
содержащую файл `.ipynb` и выполните команду:

```
jupyter notebook
```

Автоматически откроется окно браузера, где можно посмотреть интересующий документ.



