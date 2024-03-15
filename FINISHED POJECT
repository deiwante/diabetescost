CREATE DATABASE project4;
USE project4;


-- full joined databases 

SELECT dc.`2011`, dc.`2021`, r.readmitted
FROM diabetescost AS dc
JOIN readmittion AS r ON r.`Country_Territory` = dc.`Country_Territory`
WHERE r.readmitted = 'Yes';

-- the amount of people per gender.

SELECT gender, COUNT(age) FROM readmittion
GROUP BY gender
ORDER BY gender DESC;

-- list of genders + age and readmitted to hospitals
SELECT gender, age, readmitted FROM readmittion AS r
WHERE r.readmitted = 'Yes'
ORDER BY gender;

-- Gender Female age over 45 + readmitted to hospital
SELECT r.gender, r.age, r.readmitted 
FROM (
    SELECT gender, age, readmitted
    FROM readmittion
    WHERE readmitted = 'Yes'
) AS r
WHERE r.age > 45 AND r.gender = 'Female'
ORDER BY r.gender;

-- Female readmitted count

SELECT 
    COUNT(CASE WHEN r.gender = 'Female' THEN 1 END) AS Female_Readmitted_Count
FROM (
    SELECT gender, age, readmitted
    FROM readmittion
    WHERE readmitted = 'Yes' AND age > 45
) AS r;


-- Changed the name to make it as relationship collumn
ALTER TABLE diabetescost
CHANGE `Country_Territory` `Country_Territory` CHAR(250);
ALTER TABLE diabetescost MODIFY COLUMN Country_Territory VARCHAR(255);
ALTER TABLE readmittion MODIFY COLUMN Country_Territory VARCHAR(255);

-- def keys for 
ALTER TABLE readmittion
ADD CONSTRAINT fk_readmittion_diabetescost_CountryTerritory
    FOREIGN KEY (Country_Territory) 
    REFERENCES diabetescost(Country_Territory);

-- MIN/MAX/MEAN
SELECT 
MIN(age) AS 'Youngest',
MAX(age) AS 'Oldest',
ROUND(AVG(age),2) as 'Average'
FROM readmittion
WHERE readmitted = 'Yes';



  /*
  WHERE + 
  MIN/MAX +
  P.KEY +
  F.KEY + 
  ORDER +
  GROUP BY
  SUBQUERY +
  CASE + 
  ;\
  
  
