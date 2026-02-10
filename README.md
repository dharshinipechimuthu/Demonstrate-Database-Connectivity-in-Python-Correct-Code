# Demonstrate-Database-Connectivity-in-Python-Correct-Code
import mysql.connector

conn = mysql.connector.connect(
    host="localhost",
    user="root",
    password="",
    database="db1"
)

cursor = conn.cursor()
cursor.execute("INSERT INTO books VALUES (101, 'Python')")
conn.commit()

print("Record inserted successfully")

cursor.execute("SELECT * FROM books")
result = cursor.fetchall()
print(result)

conn.close()

Output:
Record inserted successfully
[(101, 'Python')]
