
как безопасно создавать:

	import sqlite3 as sq

	with sq.connect("название БД с расширением .db") as con:
		cur = con.cursor()     # Cursor()

		cur.execute("DROP TABLE IF EXISTS users") # удаление БД с условием если есть
		cur.execute("""CREATE TABLE IF NOT EXISTS users(
		user_id INTEGER PRIMARY KEY AUTOINCREMENT, # у всех user_id уникален
		name TEXT NOT NULL, # текст не должен быть пустым
		sex INTEGER NOT NULL DEFAULT 1, # 		
		
		)""")
		