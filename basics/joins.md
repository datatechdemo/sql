# SQL Joins 

## Inner Join
Inner join produces only the set of records that match in both Table A and Table B.
      
      SELECT * FROM tableA
      INNER JOIN tableB
      ON tableA.column_name = tableB.column_name;

<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/Inner-join.PNG">
</p>

## Left Join or Left outer join
Left outer join produces a complete set of records from Table A, with the matching records (where available) in Table B. If there is no match, the right side will contain null.

    SELECT * FROM tableA
    LEFT OUTER JOIN tableB
    ON tableA.column_name = tableB.column_name;
 
<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/left-join1.PNG">
</p>

But if you want to produce the data only from Table A, but not in Table B, we perform the same left outer join, use where clause to exclude the records we don't want from TableB.
 
    SELECT * FROM tableA
    LEFT OUTER JOIN TableB
    ON tableA.column_name = tableB.column_name
    WHERE tableB.id IS null;
 
<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/left-join2.PNG">
</p>
 
## Right Join or Right Outer Join
Right outer join produces a complete set of records from Table B, with the matching records (where available) in Table A. If there is no match, the right side will contain null.

    SELECT * FROM tableA
    Right OUTER JOIN tableB
    ON tableA.column_name = tableB.column_name;
  
<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/right-join1.PNG">
</p>  

But if you want to produce the data only from Table B, but not in Table A, we perform the same right outer join, use where clause to exclude the records we don't want from TableA.
 
    SELECT * FROM tableA
    Right OUTER JOIN tableB
    ON tableA.column_name = tableB.column_name
    WHERE tableA.id IS null;

<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/right-join2.PNG">
</p>

## Full Outer Join or Full Join
Full outer join produces the set of all records in Table A and Table B, with matching records from both sides where available. If there is no match, the missing side will contain null.

      SELECT *
      FROM tableA
      FULL OUTER JOIN tableB
      ON tableA.column_name = tableB.column_name

<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/full-outer-join1.png">
</p>
