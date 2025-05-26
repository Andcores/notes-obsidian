Las bases de datos es información que se necesita extraer por alguna razón que nos pidan o necesitemos en especifico

En las bases de datos las búsquedas las hacemos por medio de clausulas, estas miraremos la manera de búsqueda mas básica

**SELECT customerid, city, country
FROM customers
ORDER BY city;**
En estas clausulas 
From = la tabla que vamos a usar para buscar la información
Select seran las columnas que necesitamos de esta en es caso son 3
y order by va a ser le orden de como se va a organizar esta búsqueda 
El resultado de estas clausulas seria : 
+------------+--------------+----------------+ |
CustomerId | City | Country |
+------------+--------------+----------------+ 
| 48 | Amsterdam | Netherlands | 
| 59 | Bangalore | India | 
| 36 | Berlin | Germany | 
| 38 | Berlin | Germany | 
| 42 | Bordeaux | France |
| 23 | Boston | USA |
| 13 | Brasília | Brazil |
| 8 | Brussels | Belgium |
| 45 | Budapest | Hungary | 
| 56 | Buenos Aires | Argentina |
| 24 | Chicago | USA |
| 9 | Copenhagen | Denmark | 
| 19 | Cupertino | USA | 
| 58 | Delhi | India | 
| 43 | Dijon | France | 
| 46 | Dublin | Ireland | 
| 54 | Edinburgh | United Kingdom | 
| 14 | Edmonton | Canada |
| 26 | Fort Worth | USA | 
| 37 | Frankfurt | Germany |
| 31 | Halifax | Canada | 
| 44 | Helsinki | Finland | 
| 34 | Lisbon | Portugal |
| 52 | London | United Kingdom | 
| 53 | London | United Kingdom |
+------------+--------------+----------------+
(Output limit exceeded, 25 of 59 total rows shown)
**SELECT firstname, lastname, title, email
FROM employees
WHERE title = 'IT Staff';** 
En las siguientes clausulas se ven agregado el " WHERE"
Este da una búsqueda de filtrado aun mas alta pues la condicional trae información mas en especifico de una columna en especifico
+-----------+----------+----------+------------------------+
| FirstName | LastName | Title | Email |
+-----------+----------+----------+------------------------+
| Robert | King | IT Staff | robert@chinookcorp.com |
| Laura | Callahan | IT Staff | laura@chinookcorp.com |
+-----------+----------+----------+------------------------+
en este caso el trajo a la DB De la columna de " title " a las personas que estaban en IT Staff 
un comodín para usar la clausula WHERE  es LIKE donde se puede colocar antes y/o después de la cadena para diferentes resultados, en la siguiente tabla están los ejemplos de como funciona el comodín LIKE
![[Pasted image 20240805223507.png]]
**SELECT lastname, firstname, title, email
FROM employees
WHERE title LIKE 'IT%';**
+----------+-----------+------------+-------------------------+
| LastName | FirstName | Title | Email |
+----------+-----------+------------+-------------------------+
| Mitchell | Michael | IT Manager | michael@chinookcorp.com |
| King | Robert | IT Staff | robert@chinookcorp.com |
| Callahan | Laura | IT Staff | laura@chinookcorp.com |
+----------+-----------+------------+-------------------------+

**SELECT firstname, lastname, birthdate
FROM employees
WHERE birthdate > '1970-01-01';**
En las siguientes clausulas estamos dando condiciones diferentes con el WHERE donde este nos dice que en la columna de Birthdate sea mayor a la fecha X

+-----------+----------+---------------------+
| FirstName | LastName | BirthDate |
+-----------+----------+---------------------+ 
| Jane | Peacock | 1973-08-29 00:00:00 |
| Michael | Mitchell | 1973-07-01 00:00:00 |
| Robert | King | 1970-05-29 00:00:00 |
+-----------+----------+---------------------+

**SELECT firstname, lastname, hiredate
FROM employees
WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';**}

Luego de nuestra clausula WHERE encontramos otra clausula que es Between para dar un filtro entre una fecha y la otra 
	


+-----------+----------+---------------------+ 
| FirstName | LastName | HireDate |
+-----------+----------+---------------------+
| Andrew | Adams | 2002-08-14 00:00:00 |
| Nancy | Edwards | 2002-05-01 00:00:00 |
| Jane | Peacock | 2002-04-01 00:00:00 |
+-----------+----------+---------------------+

## CONDICIONALES AND OR Y NOT##

And es un filtro de 2 condiciones en la cual se deben satisfacer ambas condiciones para realizar la consulta 
**SELECT firstname, lastname, email, country, supportrepid
FROM customers
WHERE supportrepid = 5 AND country = 'USA';**
+-----------+----------+-------------------------+---------+--------------+
| FirstName | LastName | Email | Country | SupportRepId | 
+-----------+----------+-------------------------+---------+--------------+ | Jack | Smith | jacksmith@microsoft.com | USA | 5 |
| Kathy | Chase | kachase@hotmail.com | USA | 5 | 
| Victor | Stevens | vstevens@yahoo.com | USA | 5 |
| Julia | Barnett | jubarnett@gmail.com | USA | 5 |
+-----------+----------+-------------------------+---------+--------------+

OR es un filtro en el que se debe satisfacer algunas de las opciones dadas en el condicional de la consulta 


**SELECT firstname, lastname, email, country
FROM customers
WHERE country = 'Canada' OR country = 'USA';**

+-----------+------------+--------------------------+---------+ 
| FirstName | LastName | Email | Country |
+-----------+------------+--------------------------+---------+ 
| François | Tremblay | ftremblay@gmail.com | Canada | 
| Mark | Philips | mphilips12@shaw.ca | Canada |
| Jennifer | Peterson | jenniferp@rogers.ca | Canada |
| Frank | Harris | fharris@google.com | USA |
| Jack | Smith | jacksmith@microsoft.com | USA |
| Michelle | Brooks | michelleb@aol.com | USA | 
| Tim | Goyer | tgoyer@apple.com | USA |
| Dan | Miller | dmiller@comcast.com | USA | 
| Kathy | Chase | kachase@hotmail.com | USA | 
| Heather | Leacock | hleacock@gmail.com | USA |
| John | Gordon | johngordon22@yahoo.com | USA | |
Frank | Ralston | fralston@gmail.com | USA |
| Victor | Stevens | vstevens@yahoo.com | USA |
| Richard | Cunningham | ricunningham@hotmail.com | USA | 
| Patrick | Gray | patrick.gray@aol.com | USA |
| Julia | Barnett | jubarnett@gmail.com | USA | 
| Robert | Brown | robbrown@shaw.ca | Canada | 
| Edward | Francis | edfrancis@yachoo.ca | Canada | 
| Martha | Silk | marthasilk@gmail.com | Canada |
| Aaron | Mitchell | aaronmitchell@yahoo.ca | Canada | 
| Ellie | Sullivan | ellie.sullivan@shaw.ca | Canada |
+-----------+------------+--------------------------+---------+
Las conjugaciones de los filtros NOT se pueden conjugar con los AND para hacer clausulas y consultas mas especificas 


# Join
Los join es basicamente combinar tablas entre si 
tenemos diferentes tipos de join y aqui esta el primero 
## INNER JOIN
![[Pasted image 20240930215213.png]]
*SELECT *
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;* 
esta es la sintaxis del inner join
el on luego de inner join es para espesificar que tabla se va a unir 

## LEFT JOIN
![[Pasted image 20240930220222.png]]
Su funcionamiento basicamente es selecionar datos que unen a a ambas tablas y la tabla dela izquierda "se podria decir que el JOIN es la parte media entonces lo que este a la izquierda del join es la tabla izquierda, igualmente para la derecha"

*SELECT *
FROM employees
LEFT JOIN machines ON employees.device_id = machines.device_id;*


## RIGHT JOIN
![[Pasted image 20240930220412.png]]

Es igual al left join diferencia es que selecciona la tabla de la derecha 

*SELECT *
FROM employees
RIGHT JOIN machines ON employees.device_id = machines.device_id;*

## FULL OUTER JOIN
![[Pasted image 20240930220602.png]]
Este join engloba todo lo de ambas tablas

*SELECT *
FROM employees
FULL OUTER JOIN machines ON employees.device_id = machines.device_id;*
