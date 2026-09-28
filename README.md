1. Create the Restaurants table and insert 5 sample records
CREATE TABLE Restaurants (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    cuisine VARCHAR(50),
    rating DECIMAL(2, 1),
    city VARCHAR(50)
);

INSERT INTO Restaurants (id, name, cuisine, rating, city) VALUES
(1, 'Swati Snacks', 'Gujarati', 4.5, 'Ahmedabad'),
(2, 'Swagat Restaurant', 'South Indian', 4.2, 'Surat'),
(3, 'Caffe Italia', 'Italian', 3.8, 'Ahmedabad'),
(4, 'The Dragon House', 'Chinese', 4.1, 'Vadodara'),
(5, 'Swadisht Bhojanalay', 'North Indian', 3.4, 'Surat');


2. Rating  4.0 in either Ahmedabad or Surat
SELECT * 
FROM Restaurants
WHERE rating > 4.0 
  AND city IN ('Ahmedabad', 'Surat');

3. -- 3. Restaurant names starting with 'Swa'
SELECT * 
FROM Restaurants
WHERE name LIKE 'Swa%';


4. Rating between 3.5 and 4.5
SELECT * 
FROM Restaurants
WHERE rating BETWEEN 3.5 AND 4.5;

 5. Cuisine is Chinese, Italian, or South Indian
SELECT * 
FROM Restaurants
WHERE cuisine IN ('Chinese', 'Italian', 'South Indian');
