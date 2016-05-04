# Basic-Teradata
Just basic Teradata queries

//General


HELP TABLE skstinfo

//Selecting data


SELECT TOP 10*
FROM deptinfo

SELECT *
FROM trnsact
SAMPLE .10
ORDER BY SALEDATE ASC

SELECT amt, sprice 
FROM trnsact
WHERE amt <> sprice

SELECT cost, retail
FROM skstinfo
WHERE cost='0' AND retail='0'

//Summarising data


SELECT COUNT(SKU)
FROM trnsact

SELECT COUNT(DISTINCT SKU)
FROM trsnact

SELECT COUNT(DISTINCT SKU)
FROM trnsact
WHERE SALEDATE > 05/01/01

SELECT AVG(SPRICE)
FROM trnsact

//Grouping and summarising


SELECT sku, COUNT(sku), AVG(retail), AVG(cost)
FROM skstinfo
GROUP BY sku;



