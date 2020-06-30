# sql-afternoon-project-1


Table - person


-- CREATE TABLE person (
--   person_id SERIAL,
--   full_name VARCHAR(100), 
--   age INT,
--   height INT,
--   city TEXT,
--   favorite_color TEXT

--   );
  

INSERT INTO person
(full_name, favorite_color, city, height, age)

VALUES ('Lebron James', 'blue', 'Los Angeles', 198, 30), 
('James Harden', 'red', 'Houston',  180, 27),
('Kawhi Leonard', 'yellow', 'Los Angeles', 185, 25),
('JJ Reddick', 'green', 'New Orleans', 174, 35),
('Kevin Durant', 'orange', 'New Jersey', 200, 29);


-- SELECT * FROM person
-- ORDER BY height DESC

-- SELECT * FROM person
-- ORDER BY height ASC

-- SELECT * FROM person
-- ORDER BY age DESC

-- SELECT * FROM person
-- WHERE age > 20

-- SELECT * FROM person
-- WHERE age = 18;

-- SELECT * FROM person
-- WHERE age < 20 AND age > 30;

-- SELECT * FROM person 
-- WHERE age != 27;

-- SELECT * FROM person
-- WHERE favorite_color != 'red'

-- SELECT * FROM person
-- WHERE favorite_color != 'red' AND favorite_color != 'blue';

-- SELECT * FROM person
-- WHERE favorite_color = 'orange' OR favorite_color ='green';

-- SELECT * FROM person
-- WHERE favorite_color IN ('orange', 'green', 'blue')

-- SELECT * FROM person
-- WHERE favorite_color IN ('yellow', 'purple')



Table-orders

CREATE TABLE records (
  
  order_id SERIAL,
  person_id SERIAL,
  product_name VARCHAR(100),
  product_price INT,
  quantity INT

);


INSERT INTO records 
(product_name, quantity, product_price)
VALUES 

('Computer', 20, 999), 
('Phone', 5, 400),
('Car', 2, 1500),
('Boat',17, 26),
('Drone', 99, 127);

-- SELECT * FROM records


-- SELECT sum(quantity) AS orders FROM records

-- SELECT product_name, (product_price * quantity) AS total_order_price FROM records

-- SELECT person_id, (product_price * quantity) AS total_order FROM records

-- SELECT sum(product_price * quantity) FROM records
-- WHERE person_id = 3




Table- artists 

INSERT INTO artist (name)
VALUES ('Kygo'), ('Drake'), ('The Chainsmokers');

-- SELECT name FROM artist
-- ORDER BY name desc
-- LIMIT 10

-- SELECT name FROM artist
-- ORDER BY name asc
-- LIMIT 5

-- SELECT * FROM artist
-- WHERE name LIKE 'Black%'

-- SELECT * FROM artist
-- WHERE name LIKE '%Black%'











Table - Employee

-- SELECT first_name, last_name, city FROM employee
-- WHERE city = 'Calgary'

-- SELECT first_name, last_name, birth_date FROM employee
-- ORDER BY birth_date DESC
-- limit 1

-- SELECT first_name, last_name, birth_date FROM employee
-- ORDER BY birth_date ASC
-- limit 1

-- SELECT first_name, last_name, reports_to FROM employee
-- WHERE reports_to = 2

-- SELECT count(city) FROM employee
-- WHERE city = 'Lethbridge'




Table - invoice

-- SELECT count(billing_country) FROM invoice
-- WHERE billing_country = 'USA'


-- SELECT DISTINCT(total) FROM invoice
-- ORDER BY total desc
-- limit 1

-- SELECT DISTINCT(total) FROM invoice
-- ORDER BY total asc
-- limit 1

-- SELECT DISTINCT(total) FROM invoice
-- WHERE total >= 5
-- ORDER BY total asc

-- SELECT count(total) FROM invoice
-- WHERE total < 5

-- SELECT count(total) FROM invoice
-- WHERE billing_state IN ('CA', 'TX', 'AZ')

-- SELECT avg(total) FROM invoice

-- SELECT sum(total) FROM invoice
