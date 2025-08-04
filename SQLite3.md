
как безопасно создавать:

	import sqlite3 as sq

	with sq.connect("название БД с расширением .db") as con:
		cur = con.cursor()     # Cursor()

		con.execute("DROP TABLE IF EXISTS users")
	