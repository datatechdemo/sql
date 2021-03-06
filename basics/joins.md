# SQL Joins 

## Inner Join
Inner join produces only the set of records that match in both Table A and Table B.
      
      SELECT * FROM tableA
      INNER JOIN tableB
      ON tableA.column_name = tableB.column_name;

<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/images/Inner-join.PNG">
</p>

## Left Join or Left outer join
Left outer join produces a complete set of records from Table A, with the matching records (where available) in Table B. If there is no match, the right side will contain null or blank or zero (depending on the system)

    SELECT * FROM tableA
    LEFT OUTER JOIN tableB
    ON tableA.column_name = tableB.column_name;
 
<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/images/left-join1.PNG">
</p>

But if you want to produce the records only from Table A, but not in Table B, we perform the same left outer join but use where clause it will exclude all records of Table B and also records of Table A which matches with Table B.
 
    SELECT * FROM tableA
    LEFT OUTER JOIN TableB
    ON tableA.column_name = tableB.column_name
    WHERE tableB.id IS null;
 
<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/images/left-join2.PNG">
</p>
 
## Right Join or Right Outer Join
Right outer join produces a complete set of records from Table B, with the matching records (where available) in Table A. If there is no match, the right side will contain null.

    SELECT * FROM tableA
    Right OUTER JOIN tableB
    ON tableA.column_name = tableB.column_name;
  
<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/images/right-join1.PNG">
</p>  

But if you want to produce the records only from Table B, but not in Table A, we perform the same left outer join but use where clause it will exclude all records of Table A and also records of Table B which matches with Table A.
 
    SELECT * FROM tableA
    Right OUTER JOIN tableB
    ON tableA.column_name = tableB.column_name
    WHERE tableA.id IS null;

<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/images/right-join2.PNG">
</p>

## Full Outer Join or Full Join
Full outer join produces the set of all records in Table A and Table B, with matching records from both sides where available. If there is no match, the missing side will contain null or blank or zero (depending on the system)

      SELECT *
      FROM tableA
      FULL OUTER JOIN tableB
      ON tableA.column_name = tableB.column_name

<p align="center">
  <img src="https://github.com/datatechdemo/sql/blob/main/basics/images/full-outer-join2.png">
</p>
