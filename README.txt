

Установка и настройка
=====================

Установить пакет pywin32:
	pip install pywin32

Согласно источнику [https://youtu.be/UVCH_wDlFNU?t=863],
cкопировать файлы:
	Kompas6API5.py
	KompasAPI7.py
	ksConstants.py
	ksConstants3D.py
	LDefin2D.py
	LDefin3D.py
	MiscellaneousHelpers.py
из папки (путь может несколько отличаться):
	C:\ProgramData\ASCON\KOMPAS-3D\21\Python 3\App\Lib\site-packages\pythonwin
в папку (путь может несколько отличаться):
	C:\Program Files\Python39\Lib\site-packages\pythonwin



Использование
=============

1. Запустить сервер
-------------------

Команда:
	python server.py

Удобнее написать и запускать вместе с Компасом файл типа 'start_server.bat',
	в который вставить код наподобие:
C:
cd "<путь к директории установки>"
python server.py


2. Отправлять команды серверу через клиент
---------------------------

Команда:
	python client.py <command_name>

Удобнее в самом Компас-3D добавить "Утилиту":
Приложения -> Конфигуратор -> Состав -> Добавить утилиты...
Путь к файлу: C:\Program Files\Python39\python.exe
В списке приложений найти свежедобавленную утилиту "python".
Настроить следующим образом:
	Имя: произвольное, например "Основная надпись";
	Путь: должен быть "C:\Program Files\Python39\python.exe" (путь может
		несколько отличаться);
	Параметры: "<путь к директории установки>" "<название команды>"
	Описание: произвольное.
Настроить интерфейс: добавить кнопку на существующую или новую панель и/или
	назначить горячую клавишу.

Поддерживаемые названия команд:
	change_bg
	fast_mate
	drawing_stamp
	export_png
	export_pdf_2d
	export_step
	fix_LCS


