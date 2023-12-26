[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

# Вступительные слова
Весь материал представленный в этом репозитории является переводом 
материала из репозитория https://github.com/FireDynamics/LectureFireSimulation.

Перевод и адаптацию произвел Мироненко Роман Владимирович.

Открыт для предложений по переводу и сотрудничеству.

# Курс «Моделирование пожара»
Лекции и упражнения по моделированию пожара

## Веб-страница сборки
https://romanmironenko.github.io/LectureFireSimulation_RU

## Местная разработка

*Примечение: Следующие явные команды предназначены для bash / zsh на Linux / MacOS.*

### 1. Клонировать репозиторий
```
git clone https://github.com/RomanMironenko/LectureFireSimulation_RU.git
```
### 2. Внутри репозитория настройте виртуальное окружение для Python.
```
python -m venv .venv
```
### 3. Активируйте виртуальное окружение
```
source .venv/bin/activate
```

Требования к различным системам, см. [link](https://docs.python.org/3/library/venv.html):

| Платформа |    Оболочка     | Команда активации виртуального окружения |
| -------- |:---------------:|------------------------------------------|
| POSIX    |    bash/zsh     | $ source <venv>/bin/activate             |
|          |      fish       | $ source <venv>/bin/activate.fish        |
|          |    csh/tcsh     | $ source <venv>/bin/activate.csh         |
|          | PowerShell Core | $ <venv>/bin/Activate.ps1                |
| Windows  |     cmd.exe     | C:\> <venv>\Scripts\activate.bat         |
|          |   PowerShell    | PS C:\> <venv>\Scripts\Activate.ps1      |

Примечение: В Windows PowerShell существует ограничение на запуск скриптов. Если политика выполнения не изменена, появится сообщение типа «невозможно загрузить, поскольку в этой системе отключено выполнение сценариев». Можно разрешить выполнение сценариев для активного сеанса PowerShell, выполнив `Set-ExecutionPolicy Unrestricted -Scope Process`, см. [link](https://stackoverflow.com/questions/18713086/virtualenv-wont-activate-on-windows).

### 4. Установите необходимые пакеты Python, необходимые только один раз.
```
pip install -r requirements.txt
```
### 5. Запустите JupyterLab.
```
jupyter-lab
```
### 6. Сделайте некоторое редактирование. Содержимое книги хранится в папке «content».
### 7. Создайте локальную версию книги
```
cd book
jupyter-book build .
```
Примечание: Некоторые блокноты способны включать и выключать вывод рисунков matplotlib на основе переменной окружения JB_NOSHOW. Ее следует установить (в любое значение), чтобы предотвратить вывод дубликатных фигур, например:

```
cd book
JB_NOSHOW=1 jupyter-book build .
```

### 8. Если сборка прошла успешно, будет указано местоположение книги сборки. Вы можете открыть ее с помощью браузера.

## Хранилище данных

Входные файлы моделирования, а также результаты моделирования хранятся в папке `data`.

### Выполнение моделирования

Во всех подпапках находятся входные файлы FDS, а также сценарий запуска `case_run.sh`. Возможно, вам придется изменить команду выполнения FDS в верхней части скрипта.

### Загрузить предварительно рассчитанные данные

Скрипт `case_download.sh` внутри отдельных подпапок можно использовать для загрузки предварительно рассчитанных данных.

## Вклад

### Для внешних

Пожалуйста, обратитесь к ветке «разработка» и создайте запрос на включение на ее основе.

### Для внутренних

**Новый раздел/контент**: создайте функциональную ветку «разработка». После завершения объедините его обратно и создайте ветку выпуска с вашими изменениями, которые необходимо отправить в `main`. Назначьте Лукаса рецензентом запроса на включение.

**Опечатки/исправления**: поместите их непосредственно в ветку разработки, а затем непосредственно в ветку main.

## Лицензия

Эта работа лицензирована под
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
