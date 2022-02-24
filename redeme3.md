
# sql  is relatioanal db
and it's  stands for
Structured Query Language
and relational db organize  it's data in tabels and you can create multi tabels in db 

## tabls
when you create table you must defind colums
and all data can row 
## Query
each comans excution in db in call query  the gole of this command is add delete, update or select data in table or more than table have relations between each ather  .
  i will presen more pepular qureys

### SELECT
to select spesific data from the table
 syntaics:
 SELECT columns_name FROM table_name;
in case you went to show all colums 
 SELECT * FROM table_name;


![The San Juan Mountains are beautiful!](/ass/Screenshot(34).png "San Juan Mountains")

### LIMIT
if you want to show spesfic num of row when you select use limit
SELECT * FROM columns_name LIMIT num;

![The San Juan Mountains are beautiful!](/ass/Screenshot(35).png "San Juan Mountains")
### WHERE &LIKE
if look up for spicfic data in colums usr where with it's condution
SELECT * FROM columns_name WHERE columns_name CONDUTION ;
We can use like as acondetion when we look up at same value
SELECT * FROM columns_name WHERE columns_name like "% thing%" ;

![The San Juan Mountains are beautiful!](/ass/Screenshot(36).png "San Juan Mountains")
## offset
to show the next of limmit
![The San Juan Mountains are beautiful!](/ass/Screenshot(37).png "San Juan Mountains")

## order by
to order data  besed on colome (ASC/DESC)

![The San Juan Mountains are beautiful!](/ass/Screenshot(38).png "San Juan Mountains")
## INNER JOIN
to show the common data besed on common  data in coloum
![The San Juan Mountains are beautiful!](/ass/Screenshot(39).png "San Juan Mountains")
## LEFT / RIGHT JOIN
to show the  data of teble and  the common data besed on common  data in sensand teble
![The San Juan Mountains are beautiful!](/ass/Screenshot(40).png "San Juan Mountains")
## group by
to deale whith data that cave spesific data in one colume.
![The San Juan Mountains are beautiful!](/ass/Screenshot(41).png "San Juan Mountains")
## SUM, COUNT...
method we use with group by to have data from some of colums in table
![The San Juan Mountains are beautiful!](/ass/Screenshot(42).png "San Juan Mountains")

![The San Juan Mountains are beautiful!](/ass/Screenshot(43).png "San Juan Mountains")
![The San Juan Mountains are beautiful!](/ass/Screenshot(44).png "San Juan Mountains")

## have
it work in group like where 
![The San Juan Mountains are beautiful!](/ass/Screenshot(45).png "San Juan Mountains")

## the syntaes
SELECT columns, columa AS thing, …
FROM table INNER/LEFT/RIGHT JOIN ON
WHERE condition
GROUP BY column
HAVING condition;

![The San Juan Mountains are beautiful!](/ass/Screenshot(45).png "San Juan Mountains")


