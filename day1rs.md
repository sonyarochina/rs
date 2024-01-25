# Exercise 0
```sql
SELECT pizzeria_id, pizza_name FROM menu
UNION
SELECT id, name FROM person
ORDER BY pizzeria_id, pizza_name
```
![image](https://github.com/sonyarochina/rs/assets/157011181/249dd637-3f22-444d-96e3-cb385d9640fd)

# Exercise 03
```sql
SELECT object_name FROM (
	SELECT name AS object_name, 'person' 
	FROM person
	UNION
	SELECT pizza_name, 'pizza'
	FROM menu
	ORDER BY 2, 1
) tab
```
![image](https://github.com/sonyarochina/rs/assets/157011181/8656aa16-64a9-4a86-aaf4-82be4f3947bf)

# Exercise 02
```sql
SELECT
	order_date AS action_date,
	p.name FROM person_order po
JOIN person_visits pv ON po.order_date = pv.visit_date AND po.person_id = pv.person_id
JOIN person p ON pv.person_id = p.id
```
![image](https://github.com/sonyarochina/rs/assets/157011181/5b0f39ed-9449-400f-a4f2-1621a5dbc2c6)

