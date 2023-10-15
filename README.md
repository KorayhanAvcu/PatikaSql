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

## ÖDEV 8
--1.test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
CREATE TABLE employee(
	id INTEGER,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
);

--2.Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
insert into employee (id, name, birthday, email) values (1, 'Daffy Truran', '2023-07-21', 'dtruran0@constantcontact.com');
insert into employee (id, name, birthday, email) values (2, 'Francklin Daveridge', '2023-07-01', 'fdaveridge1@un.org');
insert into employee (id, name, birthday, email) values (3, 'Ailene Vickress', '2023-03-19', 'avickress2@i2i.jp');
insert into employee (id, name, birthday, email) values (4, 'Barbara-anne Bartunek', '2023-06-26', 'bbartunek3@ezinearticles.com');
insert into employee (id, name, birthday, email) values (5, 'Salvatore Ravenscroft', '2023-06-25', 'sravenscroft4@csmonitor.com');
insert into employee (id, name, birthday, email) values (6, 'Josefina Jecks', '2023-04-06', 'jjecks5@boston.com');
insert into employee (id, name, birthday, email) values (7, 'Dwight Bomb', '2023-06-16', 'dbomb6@nih.gov');
insert into employee (id, name, birthday, email) values (8, 'Jasmin Tipple', '2023-06-07', 'jtipple7@sfgate.com');
insert into employee (id, name, birthday, email) values (9, 'Misty Matczak', '2023-04-30', 'mmatczak8@google.de');
insert into employee (id, name, birthday, email) values (10, 'Frederigo Iscowitz', '2023-08-11', 'fiscowitz9@bing.com');
insert into employee (id, name, birthday, email) values (11, 'Mitch Block', '2023-06-26', 'mblocka@drupal.org');
insert into employee (id, name, birthday, email) values (12, 'Ernestus Boxall', '2023-08-15', 'eboxallb@geocities.com');
insert into employee (id, name, birthday, email) values (13, 'Theodor Yewdall', '2023-07-11', 'tyewdallc@marriott.com');
insert into employee (id, name, birthday, email) values (14, 'Dorthea Weekes', '2023-05-12', 'dweekesd@gov.uk');
insert into employee (id, name, birthday, email) values (15, 'Quintus Birrel', '2023-06-25', 'qbirrele@mail.ru');
insert into employee (id, name, birthday, email) values (16, 'Brooke Tidman', '2023-07-02', 'btidmanf@histats.com');
insert into employee (id, name, birthday, email) values (17, 'Xena Jaze', '2022-11-22', 'xjazeg@domainmarket.com');
insert into employee (id, name, birthday, email) values (18, 'Gradey Reville', '2023-04-15', 'grevilleh@marketwatch.com');
insert into employee (id, name, birthday, email) values (19, 'Harrie Orrobin', '2023-05-24', 'horrobini@zimbio.com');
insert into employee (id, name, birthday, email) values (20, 'Deana Jaskowicz', '2023-07-11', 'djaskowiczj@cyberchimps.com');
insert into employee (id, name, birthday, email) values (21, 'Beck Martlew', '2023-07-18', 'bmartlewk@bloomberg.com');
insert into employee (id, name, birthday, email) values (22, 'Doug Silcox', '2023-07-14', 'dsilcoxl@yellowbook.com');
insert into employee (id, name, birthday, email) values (23, 'Gerick Dobbings', '2023-05-29', 'gdobbingsm@wp.com');
insert into employee (id, name, birthday, email) values (24, 'Aldus Caswall', '2023-01-18', 'acaswalln@gravatar.com');
insert into employee (id, name, birthday, email) values (25, 'Silva Cardero', '2023-07-09', 'scarderoo@foxnews.com');
insert into employee (id, name, birthday, email) values (26, 'Ravid Kundert', '2023-01-01', 'rkundertp@ovh.net');
insert into employee (id, name, birthday, email) values (27, 'Lyn Carleton', '2023-01-14', 'lcarletonq@answers.com');
insert into employee (id, name, birthday, email) values (28, 'Leisha Colgan', '2023-06-18', 'lcolganr@nyu.edu');
insert into employee (id, name, birthday, email) values (29, 'Iris Berthe', '2023-08-15', 'iberthes@imageshack.us');
insert into employee (id, name, birthday, email) values (30, 'Sharleen Reiach', '2022-11-14', 'sreiacht@blogtalkradio.com');
insert into employee (id, name, birthday, email) values (31, 'Rocky Crier', '2023-07-29', 'rcrieru@arizona.edu');
insert into employee (id, name, birthday, email) values (32, 'Lazar Kalb', '2023-05-05', 'lkalbv@shop-pro.jp');
insert into employee (id, name, birthday, email) values (33, 'Trevor Corsan', '2022-12-09', 'tcorsanw@discovery.com');
insert into employee (id, name, birthday, email) values (34, 'Nanete Durdle', '2023-08-10', 'ndurdlex@statcounter.com');
insert into employee (id, name, birthday, email) values (35, 'Roxie Bisiker', '2023-02-19', 'rbisikery@sciencedirect.com');
insert into employee (id, name, birthday, email) values (36, 'Cornelius Lean', '2022-10-08', 'cleanz@taobao.com');
insert into employee (id, name, birthday, email) values (37, 'Hans Feeley', '2022-11-06', 'hfeeley10@cnbc.com');
insert into employee (id, name, birthday, email) values (38, 'Rebekkah Fane', '2023-03-08', 'rfane11@berkeley.edu');
insert into employee (id, name, birthday, email) values (39, 'Silva Mattock', '2023-04-15', 'smattock12@github.com');
insert into employee (id, name, birthday, email) values (40, 'Tobit Jorden', '2023-05-19', 'tjorden13@upenn.edu');
insert into employee (id, name, birthday, email) values (41, 'Parnell Bunston', '2023-01-23', 'pbunston14@globo.com');
insert into employee (id, name, birthday, email) values (42, 'Idalia Edmott', '2023-01-02', 'iedmott15@merriam-webster.com');
insert into employee (id, name, birthday, email) values (43, 'Eryn Marsy', '2023-08-24', 'emarsy16@cnbc.com');
insert into employee (id, name, birthday, email) values (44, 'Herta Gregolin', '2023-05-30', 'hgregolin17@bloglovin.com');
insert into employee (id, name, birthday, email) values (45, 'Dorette Handrahan', '2023-06-20', 'dhandrahan18@51.la');
insert into employee (id, name, birthday, email) values (46, 'Kingston Breagan', '2023-03-25', 'kbreagan19@wp.com');
insert into employee (id, name, birthday, email) values (47, 'Tyrone MacDirmid', '2023-05-12', 'tmacdirmid1a@skyrock.com');
insert into employee (id, name, birthday, email) values (48, 'Thayne Conkay', '2023-05-16', 'tconkay1b@flickr.com');
insert into employee (id, name, birthday, email) values (49, 'Britta Caldecot', '2023-08-18', 'bcaldecot1c@facebook.com');
insert into employee (id, name, birthday, email) values (50, 'Artemas Budleigh', '2023-01-26', 'abudleigh1d@msn.com');

--3.Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
UPDATE employee
SET
	name = 'Oguzhan Pala'   	------------------- id si '1' olan kişinin name alanının güncellenmesi.
WHERE id=1;
-------------------
UPDATE employee
SET
	birthday ='1997-01-01',		
	email='example@com.tr'		------------------- ismi A ile başlayıp s ile biten kişilerin birthday ve email alanının güncellenmesi.
WHERE name LIKE 'A%s'
RETURNING *;
-------------------
UPDATE employee
SET 
	name ='youngEmployee'		------------------- doğum tarihi 2023-06-01 tarihinden büyük kişilerin name alanının güncellenmesi.
WHERE birthday > '2023-06-01'
RETURNING *;
-------------------
UPDATE employee
SET
	name ='Example',
	birthday='2023-01-01'		------------------- id si 10'dan 15'e kadar olan kişilerin name ve birthday alanının güncellenmesi.
WHERE id BETWEEN 10 AND 15;
--------------------
UPDATE employee
SET 
	email='example@com.tr'		------------------- email adresi '.com' ile biten kişilerin email alanının güncellenmesi.
WHERE email LIKE '%.com'
RETURNING *;

--4.Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
DELETE FROM employee
WHERE id =2;					------------------- id si '2' olan kişinin silinmesi.
--------------------
DELETE FROM employee
WHERE name ILIKE '%a%a%a%'		-------------------- name alanının içinde 3 adet büyük küçük duyarsız 'a' olan kişilerin silinmesi. 
RETURNING *;
--------------------
DELETE FROM employee
WHERE name ='Example'			-------------------- name alanı Example olan kişilerin silinmesi.
RETURNING *;
--------------------
DELETE FROM employee
WHERE id>40;					-------------------- id si 40'dan büyük olan kişilerin silinmesi.
--------------------
DELETE FROM employee
WHERE 
	(id>10 AND id<20) OR		-------------------- id si 10-20 aralığındaki veya email adresi '.net' ile bitenlerin silinmesi.
	(email LIKE '%.net')
RETURNING *;


## ÖDEV 9
1-) SELECT C.CITY , CY.COUNTRY FROM CITY C
INNER JOIN COUNTRY CY ON C.COUNTRY_ID=CY.COUNTRY_ID <br>

2-) SELECT C.FIRST_NAME, C.LAST_NAME, P.PAYMENT_ID FROM PAYMENT P
INNER JOIN CUSTOMER C ON C.CUSTOMER_ID=P.CUSTOMER_ID <br>

3-) SELECT C.FIRST_NAME, C.LAST_NAME, R.RENTAL_ID FROM RENTAL R
INNER JOIN CUSTOMER C ON C.CUSTOMER_ID=R.CUSTOMER_ID <br>

## ÖDEV 10
1-) SELECT C.CITY , CY.COUNTRY FROM CITY C
LEFT JOIN COUNTRY CY ON C.COUNTRY_ID=CY.COUNTRY_ID <br>

2-) SELECT C.FIRST_NAME, C.LAST_NAME, P.PAYMENT_ID FROM PAYMENT P
RIGHT JOIN CUSTOMER C ON C.CUSTOMER_ID=P.CUSTOMER_ID <br>

3-) SELECT C.FIRST_NAME, C.LAST_NAME, R.RENTAL_ID FROM RENTAL R
FULL JOIN CUSTOMER C ON C.CUSTOMER_ID=R.CUSTOMER_ID <br>

## ÖDEV 11
1-) (SELECT FIRST_NAME FROM ACTOR)
UNION
(SELECT FIRST_NAME FROM CUSTOMER) <br>

2-) (SELECT FIRST_NAME FROM ACTOR)
UNION ALL
(SELECT FIRST_NAME FROM CUSTOMER) <br>

3-) (SELECT FIRST_NAME FROM ACTOR)
INTERSECT
(SELECT FIRST_NAME FROM CUSTOMER) <br>

4-) (SELECT FIRST_NAME FROM ACTOR)
INTERSECT
(SELECT FIRST_NAME FROM CUSTOMER)<br>

5-) (SELECT FIRST_NAME FROM ACTOR)
EXCEPT
(SELECT FIRST_NAME FROM CUSTOMER) <br>


6-) (SELECT FIRST_NAME FROM ACTOR)
EXCEPT ALL
(SELECT FIRST_NAME FROM CUSTOMER) <br>
<br>
## ÖDEV 12 
1-) SELECT COUNT(*) AS SONUC FROM FILM 
WHERE LENGTH > (
SELECT AVG(LENGTH) AS SONUC_2 FROM FILM
) <br>

2-)SELECT COUNT(*) AS SONUC FROM FILM
WHERE RENTAL_RATE = (SELECT MAX(RENTAL_RATE) AS SONUC FROM FILM)<br>

3-)SELECT COUNT(*) AS SONUC FROM FILM
WHERE RENTAL_RATE = (SELECT MIN(RENTAL_RATE) AS SONUC FROM FILM)
AND REPLACEMENT_COST= (SELECT MIN(REPLACEMENT_COST) AS SONUC FROM FILM)<br>

4-) SELECT CUSTOMER_ID, COUNT(*) AS TUM_ALISVERISLER FROM PAYMENT
GROUP BY CUSTOMER_ID
ORDER BY TUM_ALISVERISLER DESC<br>

