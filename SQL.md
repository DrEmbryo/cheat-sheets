Вставка в БД   
`INSERT INTO table_name (field_1,field_2) VALUES (1_value,2_value);`

---

Обновлениее данных в БД   
`UPDATE table_name SET = "new_value" WHERE field_to_change;`

---

Удаление данных из БД   
`DELETE FROM table_name WHERE field_to_delete;`

---

Изменение таблиц   
`ALTER TABEL tabel_name ADD name_of_new_col VARCHAR;` - добавить колонку в таблицу   
`ALTER TABEL tabel_name MODIFY COLUM name_of_cal INT(max_char);` - изменть колонку   
`ALTER TABEL tabel_name DROP COLUM name_of_cal;` - удалить колонку   

---

Выборка   
`SELECT * FROM tabel_name;` - выбрать все   
`SELECT * FROM tabel_name WHERE primary_key_field = value;` - найти по значению   
`SELECT * FROM tabel_name ORDER BY field;` - отсортировать по полю   
`SELECT DISTINCT field FROM tabel_name;` - выбрать без повторений   
`SELECT * FROM tabel_name WHERE field < value;` - выборка с условием   

SQL операторы    

`=` - равно - author="someone"   
`<>`- не равно - field<>"somthing"   
`BETWEEN` - значение между - cost BETWEEN 1 AND 10    
`LIKE` - совпадает с патерном - name LIKE 'Will%'       
`IN` - равно 1 или более значений - zipcode IN (1,2,3)   
`IS` - сравнение с 0  - address IS NOT NULL   
`AS` - смена имени при выводе группы - SELECT employee AS 'Department_1'

---

Индексы   
`CREATE INDEX name ON tabel_name (colum);` - добавить индекс   
`DROP INDEX name ON tabel_name;` - удалить индекс   

---

Ключи   
`FOREIGN KEY (field) REFERENCES tabel_name (field)` - добавить ключ соеденяющий значения из 2х таблиц

---

Соединение таблец   
`SELECT table_1_name.field , table_2_name.field FROM table_1_name INNER JOIN table_2_name ON table_1_name.field = table_2_name.field ORDER BY table_1_name.field`   
`SELECT table_name CONCAT (field_1, ' ' , field_2) AS 'new_col_name';` - соеденить в новую колонку   

---

Подсчеты   
`SELECT AVG(field)` - среднее значение   
`SELECT COUNT (field) table_name` - число совпадений с условием   
`SELECT max (field) table_name` - максимальное значение   
`SELECT min (field) table_name` - минимальное значение   
`SELECT sum (field) table_name` - сложить значения    
`SELECT UCASE (field) FROM table_name` - в верхний регистр   
`SELECT LCASE (field) FROM table_name` - в нижний регистр   
