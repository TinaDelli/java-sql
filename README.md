# java-sql

A student that completes this project shows that they can:
* Query data from a single table
* Query data from multiple tables
* Create a new datadaase using PostgreSQL

# Introduction

Working with SQL

# Instructions

Surf to [SQL Try Editor at W3Schools.com](https://www.w3schools.com/Sql/tryit.asp?filename=trysql_select_top)  
Answer the following data queries. Keep track of the SQL you write by pasting it into this document under its appropriate header below. You will be submitting that through the regular fork, change, pull process.

### **Clicking the `Restore Database` button in the page will repopulate the database with the original data and discard all changes you have made**.

### find all customers that live in London. Returns 6 records.
> This can be done with SELECT and WHERE clauses

```sql 
SELECT * 
FROM Customers
WHERE City = 'London'
```

4	Around the Horn	Thomas Hardy	120 Hanover Sq.	London	WA1 1DP	UK
11	B's Beverages	Victoria Ashworth	Fauntleroy Circus	London	EC2 5NT	UK
16	Consolidated Holdings	Elizabeth Brown	Berkeley Gardens 12 Brewery	London	WX1 6LT	UK
19	Eastern Connection	Ann Devon	35 King George	London	WX3 6FW	UK
53	North/South	Simon Crowther	South House 300 Queensbridge	London	SW7 1RZ	UK
72	Seven Seas Imports	Hari Kumar	90 Wadhurst Rd.	London	OX15 4NB	UK

### find all customers with postal code 1010. Returns 3 customers.
> This can be done with SELECT and WHERE clauses

```sql 
SELECT * 
FROM Customers
WHERE PostalCode = '1010'
```

12	Cactus Comidas para llevar	Patricio Simpson	Cerrito 333	Buenos Aires	1010	Argentina
54	Océano Atlántico Ltda.	Yvonne Moncada	Ing. Gustavo Moncada 8585 Piso 20-A	Buenos Aires	1010	Argentina
64	Rancho grande	Sergio Gutiérrez	Av. del Libertador 900	Buenos Aires	1010	Argentina

### find the phone number for the supplier with the id 11. Should be (010) 9984510.
> This can be done with SELECT and WHERE clauses

```sql 
SELECT Phone
FROM Suppliers
WHERE SupplierID = '11'
```

11	Heli Süßwaren GmbH & Co. KG	Petra Winkler	Tiergartenstraße 5	Berlin	10785	Germany	(010) 9984510

Phone
(010) 9984510

### list orders descending by the order date. The order with date 1997-02-12 should be at the top.
> This can be done with SELECT, WHERE, and ORDER BY clauses


```sql 
SELECT * 
FROM Orders
ORDER BY OrderDate desc
```

10443	66	8	1997-02-12	1
10442	20	3	1997-02-11	2
10440	71	4	1997-02-10	2
10441	55	3	1997-02-10	2
10439	51	6	1997-02-07	3
10438	79	3	1997-02-06	2
10436	7	3	1997-02-05	2
10437	87	8	1997-02-05	1
10435	16	8	1997-02-04	2
10433	60	3	1997-02-03	3
10434	24	3	1997-02-03	2
10432	75	3	1997-01-31	2
10430	20	4	1997-01-30	1
10431	10	4	1997-01-30	2
10429	37	3	1997-01-29	2
10428	66	7	1997-01-28	1
10426	29	4	1997-01-27	1
10427	59	4	1997-01-27	2
10425	41	6	1997-01-24	2
10423	31	6	1997-01-23	3
10424	51	7	1997-01-23	2
10422	27	2	1997-01-22	1
10420	88	3	1997-01-21	1
10421	61	8	1997-01-21	1
10419	68	4	1997-01-20	2
10418	63	4	1997-01-17	1
10416	87	8	1997-01-16	3
10417	73	4	1997-01-16	3
10415	36	3	1997-01-15	1
10413	41	3	1997-01-14	2
10414	21	2	1997-01-14	3
10412	87	8	1997-01-13	2
10410	10	3	1997-01-10	3
10411	10	9	1997-01-10	3
10409	54	3	1997-01-09	1
10408	23	8	1997-01-08	1
10406	62	7	1997-01-07	1
10407	56	2	1997-01-07	2
10405	47	1	1997-01-06	1
10403	20	4	1997-01-03	3
10404	49	2	1997-01-03	1
10402	20	8	1997-01-02	2
10400	19	1	1997-01-01	3
10401	65	1	1997-01-01	1
10399	83	8	1996-12-31	3
10398	71	2	1996-12-30	3
10396	25	1	1996-12-27	3
10397	60	5	1996-12-27	1
10395	35	6	1996-12-26	1
10393	71	1	1996-12-25	3
10394	36	1	1996-12-25	3
10392	59	2	1996-12-24	3
10390	20	6	1996-12-23	1
10391	17	3	1996-12-23	3
10389	10	4	1996-12-20	2
10388	72	2	1996-12-19	1
10386	21	9	1996-12-18	3
10387	70	1	1996-12-18	2
10385	75	1	1996-12-17	2
10383	4	8	1996-12-16	3
10384	5	3	1996-12-16	3
10382	20	4	1996-12-13	1
10380	37	8	1996-12-12	3
10381	46	3	1996-12-12	3
10379	61	2	1996-12-11	1
10378	24	5	1996-12-10	3
10376	51	1	1996-12-09	2
10377	72	1	1996-12-09	3
10375	36	3	1996-12-06	2
10373	37	4	1996-12-05	3
10374	91	1	1996-12-05	3
10372	62	5	1996-12-04	2
10370	14	6	1996-12-03	2
10371	41	1	1996-12-03	1
10369	75	8	1996-12-02	2
10368	20	2	1996-11-29	2
10366	29	8	1996-11-28	2
10367	83	7	1996-11-28	3
10365	3	3	1996-11-27	2
10363	17	4	1996-11-26	3
10364	19	1	1996-11-26	1
10362	9	3	1996-11-25	1
10360	7	4	1996-11-22	3
10361	63	1	1996-11-22	2
10359	72	5	1996-11-21	3
10358	41	5	1996-11-20	1
10357	46	1	1996-11-19	3
10356	86	6	1996-11-18	2
10355	4	6	1996-11-15	1
10354	58	8	1996-11-14	3
10353	59	7	1996-11-13	3
10352	28	3	1996-11-12	3
10350	41	6	1996-11-11	2
10351	20	1	1996-11-11	1
10349	75	7	1996-11-08	1
10348	86	4	1996-11-07	2
10347	21	4	1996-11-06	3
10346	65	3	1996-11-05	3
10345	63	2	1996-11-04	2
10344	89	4	1996-11-01	2
10343	44	4	1996-10-31	1
10342	25	4	1996-10-30	2
10340	9	1	1996-10-29	3
10341	73	7	1996-10-29	3
10339	51	2	1996-10-28	2
10338	55	4	1996-10-25	3
10337	25	4	1996-10-24	3
10336	60	7	1996-10-23	2
10335	37	7	1996-10-22	2
10334	84	8	1996-10-21	2
10333	87	5	1996-10-18	3
10332	51	3	1996-10-17	2
10330	46	3	1996-10-16	1
10331	9	9	1996-10-16	1
10329	75	4	1996-10-15	2
10328	28	4	1996-10-14	3
10327	24	2	1996-10-11	1
10326	8	4	1996-10-10	2
10325	39	1	1996-10-09	3
10324	71	9	1996-10-08	1
10323	39	4	1996-10-07	1
10322	58	7	1996-10-04	3
10320	87	5	1996-10-03	3
10321	38	3	1996-10-03	2
10319	80	7	1996-10-02	3
10318	38	8	1996-10-01	2
10317	48	6	1996-09-30	1
10316	65	1	1996-09-27	3
10315	38	4	1996-09-26	2
10314	65	1	1996-09-25	2
10313	63	2	1996-09-24	2
10312	86	2	1996-09-23	2
10310	77	8	1996-09-20	2
10311	18	1	1996-09-20	3
10309	37	3	1996-09-19	1
10308	2	7	1996-09-18	3
10307	48	2	1996-09-17	2
10306	69	1	1996-09-16	3
10305	55	8	1996-09-13	3
10304	80	1	1996-09-12	2
10303	30	7	1996-09-11	2
10302	76	4	1996-09-10	2
10300	49	2	1996-09-09	2
10301	86	8	1996-09-09	2
10299	67	4	1996-09-06	2
10298	37	6	1996-09-05	2
10297	7	5	1996-09-04	2
10296	46	6	1996-09-03	1
10295	85	2	1996-09-02	2
10294	65	4	1996-08-30	2
10293	80	1	1996-08-29	3
10292	81	1	1996-08-28	2
10290	15	8	1996-08-27	1
10291	61	6	1996-08-27	2
10289	11	7	1996-08-26	3
10288	66	4	1996-08-23	1
10287	67	8	1996-08-22	3
10286	63	8	1996-08-21	3
10285	63	1	1996-08-20	2
10284	44	4	1996-08-19	1
10283	46	3	1996-08-16	3
10282	69	4	1996-08-15	1
10280	5	2	1996-08-14	1
10281	69	4	1996-08-14	1
10279	44	8	1996-08-13	2
10278	5	8	1996-08-12	2
10277	52	2	1996-08-09	3
10276	80	8	1996-08-08	3
10275	49	1	1996-08-07	1
10274	85	6	1996-08-06	1
10273	63	3	1996-08-05	3
10272	65	6	1996-08-02	2
10270	87	1	1996-08-01	1
10271	75	6	1996-08-01	2
10269	89	5	1996-07-31	1
10268	33	8	1996-07-30	3
10267	25	4	1996-07-29	1
10266	87	3	1996-07-26	3
10265	7	2	1996-07-25	1
10264	24	6	1996-07-24	3
10263	20	9	1996-07-23	3
10262	65	8	1996-07-22	3
10260	55	4	1996-07-19	1
10261	61	4	1996-07-19	2
10259	13	4	1996-07-18	3
10258	20	1	1996-07-17	1
10257	35	4	1996-07-16	3
10256	88	3	1996-07-15	2
10255	68	9	1996-07-12	3
10254	14	5	1996-07-11	2
10253	34	3	1996-07-10	2
10252	76	4	1996-07-09	2
10250	34	4	1996-07-08	2
10251	84	3	1996-07-08	1
10249	81	6	1996-07-05	1
10248	90	5	1996-07-04	3

### find all suppliers who have names longer than 20 characters. You can use `length(SupplierName)` to get the length of the name. Returns 11 records.
> This can be done with SELECT and WHERE clauses

```sql 
SELECT * 
FROM Suppliers
WHERE length(SupplierName) > 20
```

2	New Orleans Cajun Delights	Shelley Burke	P.O. Box 78934	New Orleans	70117	USA	(100) 555-4822
3	Grandma Kelly's Homestead	Regina Murphy	707 Oxford Rd.	Ann Arbor	48104	USA	(313) 555-5735
5	Cooperativa de Quesos 'Las Cabras'	Antonio del Valle Saavedra	Calle del Rosal 4	Oviedo	33007	Spain	(98) 598 76 54
8	Specialty Biscuits, Ltd.	Peter Wilson	29 King's Way	Manchester	M14 GSD	UK	(161) 555-4448
10	Refrescos Americanas LTDA	Carlos Diaz	Av. das Americanas 12.890	São Paulo	5442	Brazil	(11) 555 4640
11	Heli Süßwaren GmbH & Co. KG	Petra Winkler	Tiergartenstraße 5	Berlin	10785	Germany	(010) 9984510
12	Plutzer Lebensmittelgroßmärkte AG	Martin Bein	Bogenallee 51	Frankfurt	60439	Germany	(069) 992755
13	Nord-Ost-Fisch Handelsgesellschaft mbH	Sven Petersen	Frahmredder 112a	Cuxhaven	27478	Germany	(04721) 8713
14	Formaggi Fortini s.r.l.	Elio Rossi	Viale Dante, 75	Ravenna	48100	Italy	(0544) 60323
18	Aux joyeux ecclésiastiques	Guylène Nodier	203, Rue des Francs-Bourgeois	Paris	75004	France	(1) 03.83.00.68
19	New England Seafood Cannery	Robb Merchant	Order Processing Dept. 2100 Paul Revere Blvd.	Boston	02134	USA	(617) 555-3267

### find all customers that include the word "market" in the name. Should return 4 records.
> This can be done with SELECT and a WHERE clause using the LIKE keyword

> Don't forget the wildcard '%' symbols at the beginning and end of your substring to denote it can appear anywhere in the string in question

```sql 
SELECT * 
FROM Customers
WHERE CustomerName LIKE '%market%'
```

10	Bottom-Dollar Marketse	Elizabeth Lincoln	23 Tsawassen Blvd.	Tsawassen	T2F 8M4	Canada
32	Great Lakes Food Market	Howard Snyder	2732 Baker Blvd.	Eugene	97403	USA
71	Save-a-lot Markets	Jose Pavarotti	187 Suffolk Ln.	Boise	83720	USA
89	White Clover Markets	Karl Jablonski	305 - 14th Ave. S. Suite 3B	Seattle	98128	USA

### add a customer record for _"The Shire"_, the contact name is _"Bilbo Baggins"_ the address is _"1 Hobbit-Hole"_ in _"Bag End"_, postal code _"111"_ and the country is _"Middle Earth"_.
> This can be done with the INSERT INTO clause

```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('The Shire', 'Bilbio Baggins', '1 Hobbit Hole', 'Bag End', '111', 'Middle Earth')
```

You have made changes to the database. Rows affected: 1
92	The Shire	Bilbio Baggins	1 Hobbit Hole	Bag End	111	Middle Earth

### update _Bilbo Baggins_ record so that the postal code changes to _"11122"_.
> This can be done with UPDATE and WHERE clauses

```sql
UPDATE Customers
SET ContactName = 'Bilbo Baggins', PostalCode = '11122'
WHERE CustomerID = '11'
```

You have made changes to the database. Rows affected: 1
92	The Shire	Bilbo Baggins	1 Hobbit Hole	Bag End	11122	Middle Earth

### list orders grouped by customer showing the number of orders per customer. _Rattlesnake Canyon Grocery_ should have 7 orders.
> This can be done with SELECT, COUNT, JOIN and GROUP BY clauses. Your count should focus on a field in the Orders table, not the Customer table

> There is more information about the COUNT clause on [W3 Schools](https://www.w3schools.com/sql/sql_count_avg_sum.asp)

```sql
SELECT o.OrderDate, c.CustomerName, c.ContactName,
(SELECT COUNT(o.OrderID)
FROM Orders o
WHERE o.CustomerID = c.CustomerID) as ordercount
FROM Customers c JOIN Orders o
ON o.CustomerID = c.CustomerID
GROUP BY c.CustomerName
ORDER BY o.OrderDate
```
1996-07-04	Wilman Kala	Matti Karttunen	1
1996-07-05	Tradição Hipermercados	Anabela Domingues	2
1996-07-08	Hanari Carnes	Mario Pontes	2
1996-07-08	Victuailles en stock	Mary Saveley	2
1996-07-09	Suprêmes délices	Pascale Cartrain	2
1996-07-11	Chop-suey Chinese	Yang Wang	2
1996-07-12	Richter Supermarkt	Michael Holz	2
1996-07-15	Wellington Importadora	Paula Parente	2
1996-07-16	HILARIÓN-Abastos	Carlos Hernández	2
1996-07-17	Ernst Handel	Roland Mendel	10
1996-07-18	Centro comercial Moctezuma	Francisco Chang	1
1996-07-19	Old World Delicatessen	Rene Phillips	4
1996-07-19	Que Delícia	Bernardo Batista	4
1996-07-22	Rattlesnake Canyon Grocery	Paula Wilson	7
1996-07-24	Folk och fä HB	Maria Larsson	4
1996-07-25	Blondel père et fils	Frédérique Citeaux	4
1996-07-26	Wartian Herkku	Pirkko Koskitalo	7
1996-07-29	Frankenversand	Peter Franken	4
1996-07-30	GROSELLA-Restaurante	Manuel Pereira	1
1996-07-31	White Clover Markets	Karl Jablonski	2
1996-08-01	Split Rail Beer & Ale	Art Braunschweiger	6
1996-08-05	QUICK-Stop	Horst Kloss	7
1996-08-06	Vins et alcools Chevalier	Paul Henriot	2
1996-08-07	Magazzini Alimentari Riuniti	Giovanni Rovelli	3
1996-08-08	Tortuga Restaurante	Miguel Angel Paolino	4
1996-08-09	Morgenstern Gesundkost	Alexander Feuer	1
1996-08-12	Berglunds snabbköp	Christina Berglund	3
1996-08-13	Lehmanns Marktstand	Renate Messner	3
1996-08-14	Romero y tomillo	Alejandra Camino	3
1996-08-16	LILA-Supermercado	Carlos González	5
1996-08-22	Ricardo Adocicados	Janete Limeira	2
1996-08-23	Reggiani Caseifici	Maurizio Moroni	3
1996-08-26	B's Beverages	Victoria Ashworth	1
1996-08-27	Comércio Mineiro	Pedro Afonso	1
1996-09-05	Hungry Owl All-Night Grocers	Patricia McKenna	6
1996-09-09	Die Wandernde Kuh	Rita Müller	4
1996-09-11	Godos Cocina Típica	José Pedro Freyre	1
1996-09-17	Lonesome Pine Restaurant	Fran Wilson	2
1996-09-18	Ana Trujillo Emparedados y helados	Ana Trujillo	1
1996-09-20	Du monde entier	Janine Labrune	1
1996-09-20	The Big Cheese	Liz Nixon	1
1996-09-26	Island Trading	Helen Bennett	3
1996-10-04	Pericles Comidas clásicas	Guillermo Fernández	2
1996-10-07	Königlich Essen	Philip Cramer	2
1996-10-08	Save-a-lot Markets	Jose Pavarotti	4
1996-10-10	Bólido Comidas preparadas	Martín Sommer	1
1996-10-14	Furia Bacalhau e Frutos do Mar	Lino Rodriguez	2
1996-10-16	Bon app'	Laurence Lebihans	3
1996-10-17	Mère Paillarde	Jean Fresnière	5
1996-10-23	Princesa Isabel Vinhoss	Isabel de Castro	3
1996-10-29	Simons bistro	Jytte Petersen	2
1996-11-06	Familia Arquibaldo	Aria Cruz	3
1996-11-11	La maison d'Asie	Annette Roulet	5
1996-11-13	Piccolo und mehr	Georg Pipps	3
1996-11-15	Around the Horn	Thomas Hardy	2
1996-11-21	Seven Seas Imports	Hari Kumar	3
1996-11-26	Drachenblut Delikatessend	Sven Ottlieb	2
1996-11-26	Eastern Connection	Ann Devon	2
1996-11-27	Antonio Moreno Taquería	Antonio Moreno	1
1996-11-28	Galería del gastrónomo	Eduardo Saavedra	2
1996-11-28	Vaffeljernet	Palle Ibsen	2
1996-12-04	Queen Cozinha	Lúcia Carvalho	2
1996-12-05	Wolski	Zbyszek	1
1996-12-06	Hungry Coyote Import Store	Yoshi Latimer	3
1996-12-18	Santé Gourmet	Jonas Bergulfsen	1
1996-12-20	Bottom-Dollar Marketse	Elizabeth Lincoln	4
1997-01-06	LINO-Delicateses	Felipe Izquierdo	1
1997-01-07	Ottilies Käseladen	Henriette Pfalzheim	1
1997-01-08	Folies gourmandes	Martine Rancé	1
1997-01-09	Océano Atlántico Ltda.	Yvonne Moncada	1
1997-01-22	Franchi S.p.A.	Paolo Accorti	1
1997-01-23	Gourmet Lanchonetes	André Fonseca	1
1997-02-04	Consolidated Holdings	Elizabeth Brown	1
1997-02-06	Toms Spezialitäten	Karin Josephs	1

### list customers names and the number of orders per customer. Sort the list by number of orders in descending order. _Ernst Handel_ should be at the top with 10 orders followed by _QUICK-Stop_, _Rattlesnake Canyon Grocery_ and _Wartian Herkku_ with 7 orders each.
> This can be done by adding an ORDER BY clause to the previous answer

```sql 
SELECT o.OrderDate, c.CustomerName, c.ContactName,
(SELECT COUNT(o.OrderID)
FROM Orders o
WHERE o.CustomerID = c.CustomerID) as ordercount
FROM Customers c JOIN Orders o
ON o.CustomerID = c.CustomerID
GROUP BY c.CustomerName
ORDER BY ordercount desc
```

### list orders grouped by customer's city showing number of orders per city. Returns 58 Records with _Aachen_ showing 2 orders and _Albuquerque_ showing 7 orders.
> This is very similar to the previous two queries, however, it focuses on the City rather than the CustomerName

```sql
SELECT o.OrderDate, c.City,
(SELECT COUNT(o.OrderID)
FROM Orders o
WHERE o.CustomerID = c.CustomerID) as ordercount
FROM Customers c JOIN Orders o
ON o.CustomerID = c.CustomerID
GROUP BY c.City
ORDER BY ordercount desc
```

1996-07-17	Graz	10
1996-07-22	Albuquerque	7
1996-08-05	Cunewalde	7
1996-07-26	Oulu	7
1996-09-05	Cork	6
1996-08-01	Lander	6
1996-08-16	Barquisimeto	5
1996-10-17	Montréal	5
1996-11-11	Toulouse	5
1996-07-19	Anchorage	4
1996-10-08	Boise	4
1996-07-24	Bräcke	4
1996-07-29	München	4
1996-07-25	Strasbourg	4
1996-09-09	Stuttgart	4
1996-12-20	Tsawassen	4
1996-08-07	Bergamo	3
1996-09-26	Cowes	3
1996-12-06	Elgin	3
1996-08-13	Frankfurt a.M.	3
1996-08-12	Luleå	3
1996-08-14	Madrid	3
1996-10-16	Marseille	3
1996-08-23	Reggio Emilia	3
1996-11-13	Salzburg	3
1996-11-26	Aachen	2
1996-11-28	Barcelona	2
1996-07-11	Bern	2
1996-10-07	Brandenburg	2
1996-07-09	Charleroi	2
1996-07-12	Genève	2
1996-10-29	København	2
1996-10-14	Lisboa	2
1996-07-08	Lyon	2
1996-09-17	Portland	2
1996-08-06	Reims	2
1996-07-15	Resende	2
1996-07-08	Rio de Janeiro	2
1996-07-16	San Cristóbal	2
1996-07-31	Seattle	2
1996-07-05	São Paulo	2
1996-11-28	Århus	2
1997-01-09	Buenos Aires	1
1997-01-23	Campinas	1
1996-07-30	Caracas	1
1996-07-04	Helsinki	1
1997-01-06	I. de Margarita	1
1997-01-07	Köln	1
1996-08-09	Leipzig	1
1997-01-08	Lille	1
1996-08-26	London	1
1996-07-18	México D.F.	1
1997-02-06	Münster	1
1996-09-20	Nantes	1
1996-09-11	Sevilla	1
1996-12-18	Stavern	1
1997-01-22	Torino	1
1996-12-05	Walla	1

## Stretch Goals

### delete all customers that have no orders. Should delete 17 (or 18 if you haven't deleted the record added) records.
> This is done with a DELETE query

> In the WHERE clause, you can provide another list with an IN keyword this list can be the result of another SELECT query. Write a query to return a list of CustomerIDs that meet the criteria above. Pass that to the IN keyword of the WHERE clause as the list of IDs to be deleted
 
> Use a LEFT JOIN to join the Orders table onto the Customers table and check for a NULL value in the OrderID column

DELETE 
FROM Customers 
WHERE Customers.CustomerID IN (SELECT Orders.CustomerID FROM Orders WHERE Orders.CustomerID == Customers.CustomerID) = 0

## Create Database and Table

### Keep track of the code you write and paste at the end of this document

- use pgAdmin to create a database, naming it `budget`.
- add an `accounts` table with the following _schema_:

  - `id`, numeric value with no decimal places that should autoincrement.
  - `name`, string, add whatever is necessary to make searching by name faster.
  - `budget` numeric value.

- constraints
  - the `id` should be the primary key for the table.
  - account `name` should be unique.
  - account `budget` is required.

INSERT INTO accounts (name, budget)
VALUES('Bobs Burgers', 1300000)

SELECT *
FROM accounts

INSERT INTO accounts (name, budget)
VALUES('Pizza Planet', 40000000)

SELECT *
FROM accounts 

id      name            budget
integer text            integer
1       'Bobs Burgers'  1300000
2       'Pizza Planet'  40000000