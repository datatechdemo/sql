# SQL Joins 

## Inner Join
Inner join produces only the set of records that match in both Table A and Table B.
      
      SELECT * FROM TableA
      INNER JOIN TableB
      ON TableA.key = TableB.key

## Left Join or Left outer join
Left outer join produces a complete set of records from Table A, with the matching records (where available) in Table B. If there is no match, the right side will contain null.

    SELECT * FROM TableA
    LEFT OUTER JOIN TableB
    ON TableA.key = TableB.key
    
But if you want to produce the data only from Table A, but not in Table B, we perform the same left outer join, use where clause to exclude the records we don't want from TableB.
 
    SELECT * FROM TableA
    LEFT OUTER JOIN TableB
    ON TableA.name = TableB.name
    WHERE TableB.id IS null
 
## Right Join or Right Outer Join
Right outer join produces a complete set of records from Table B, with the matching records (where available) in Table A. If there is no match, the right side will contain null.

    SELECT * FROM TableA
    Right OUTER JOIN TableB
    ON TableA.key = TableB.key
    
But if you want to produce the data only from Table B, but not in Table A, we perform the same right outer join, use where clause to exclude the records we don't want from TableA.
 
    SELECT * FROM TableA
    Right OUTER JOIN TableB
    ON TableA.name = TableB.name
    WHERE TableB.id IS null
