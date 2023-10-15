# PatikaSql

## ÖDEV 1
1-) SELECT TITLE,DESCRIPTION FROM FILM <br>

2-) SELECT * FROM FILM
WHERE LENGTH>60 AND LENGTH<75 <br>

3-) SELECT * FROM FILM
WHERE RENTAL_RATE=0.99 
AND (REPLACEMENT_COST =12.99 OR REPLACEMENT_COST=28.99) <br>

4-) SELECT LAST_NAME FROM CUSTOMER 
WHERE FIRST_NAME='Mary' <br>

5-) SELECT * FROM FILM
WHERE LENGTH<50 
AND RENTAL_RATE NOT IN (2.99,4.99) <br>

## ÖDEV 2
1-) SELECT * FROM FILM
WHERE REPLACEMENT_COST BETWEEN 12.99 AND 16.99<br>

2-) SELECT FIRST_NAME, LAST_NAME FROM ACTOR
WHERE FIRST_NAME IN ('Penelope','Nick','Ed')<br>

3-) SELECT * FROM FILM
WHERE RENTAL_RATE IN (0.99,2.99,4.99) 
AND REPLACEMENT_COST IN (12.99,15.99,28.99)<br>

## ÖDEV 3
1-) SELECT * FROM COUNTRY 
WHERE COUNTRY LIKE 'A%a'<br>

2-) SELECT * FROM COUNTRY 
WHERE LENGTH(COUNTRY)>=6 AND COUNTRY LIKE '%n'<br>

3-) SELECT * FROM FILM
WHERE TITLE LIKE '%t%t%t%t%'<br>

4-) SELECT * FROM FILM
WHERE TITLE LIKE 'C%'
AND LENGTH>90 
AND RENTAL_RATE=2.99<br>

## ÖDEV 4
1-) SELECT DISTINCT(REPLACEMENT_COST) AS DEGISTIRME_UCRETI FROM FILM <br>

2-) SELECT COUNT(DISTINCT(REPLACEMENT_COST)) AS SONUC FROM FILM <br>

3-) SELECT COUNT(*) FROM FILM
WHERE TITLE LIKE 'T%' AND RATING='G' <br>

4-) SELECT COUNT(*) AS SONUC FROM COUNTRY
WHERE LENGTH(COUNTRY)=5 <br>

5-) SELECT COUNT(*) AS SONUC FROM CITY
WHERE CITY LIKE '%R' OR CITY LIKE '%r' <br>

## ÖDEV 5
1-) SELECT * FROM FILM
WHERE TITLE LIKE '%n'
ORDER BY LENGTH DESC
LIMIT 5 <br>

2-) SELECT * FROM FILM
WHERE TITLE LIKE '%n'
ORDER BY LENGTH ASC
OFFSET 5
LIMIT 5<br>

3-) SELECT * FROM CUSTOMER
WHERE STORE_ID=1
ORDER BY LAST_NAME DESC
LIMIT 4<br>

## ÖDEV 6

1-) SELECT AVG(RENTAL_RATE) AS SONUC FROM FILM

2-) SELECT COUNT(*) AS SONUC FROM FILM
WHERE TITLE LIKE 'C%'

3-) SELECT * FROM FILM
WHERE RENTAL_RATE=0.99
ORDER BY LENGTH DESC
LIMIT 1

4-) SELECT COUNT(DISTINCT(REPLACEMENT_COST)) AS SONUC FROM FILM
WHERE LENGTH > 150

## ÖDEV 7
1-) SELECT COUNT(*) AS SONUC,RATING FROM FILM
GROUP BY RATING <br>

2-) SELECT REPLACEMENT_COST, COUNT(*) AS SONUC FROM FILM
GROUP BY REPLACEMENT_COST
HAVING COUNT(*)> 50 <br>

3-) SELECT COUNT(*) AS SONUC, STORE_ID FROM CUSTOMER
GROUP BY STORE_ID <br>

4-) SELECT COUNT(*) SONUC, COUNTRY_ID FROM CITY
GROUP BY COUNTRY_ID
ORDER BY SONUC DESC
LIMIT 1 <br>
