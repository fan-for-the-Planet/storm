
04.08.2025

как безопасно создавать базу данных:

	import sqlite3 as sq

	with sq.connect("название БД с расширением .db") as con:
		cur = con.cursor()     # Cursor()

		cur.execute("DROP TABLE IF EXISTS users") # удаление БД с условием если есть
		cur.execute("""CREATE TABLE IF NOT EXISTS users(
		user_id INTEGER PRIMARY KEY AUTOINCREMENT, # у всех user_id уникален
		name TEXT NOT NULL, # текст не NULL
		sex INTEGER NOT NULL DEFAULT 1, # 	столбец sex не равен значению NULL по дефолту значение == 1
		old INTEGER, # значение должно быть числом
		score INTEGER # значение должно быть числом
		
		)""")

05.08.2025

INSERT - добавление записи в таблицу;
SELECT - выборка данных из таблиц (в том числе о при создании свободной выборки из нескольких таблиц).

чтобы заполнить таблицу пиши:
INSERT INTO <table_name>(<column_name>)