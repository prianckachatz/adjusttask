# adjusttask
min_to_max_val is the function which can take inputs: tablename and column and then will find the max and min values of the column data and dispay in text format when called as below example:

SELECT min_to_max_val
FROM 
    min_to_max_val('id','towns')
    AS t( min_to_max_val TEXT) ;
    
 Output:
 
    min_to_max_val
---------------------
 1000001 -> 11000000
(1 row)

The table DDL is:

\d towns
                                   Table "test.towns"
   Column   |         Type          |                     Modifiers
------------+-----------------------+----------------------------------------------------
 id         | integer               | not null default nextval('towns_id_seq'::regclass)
 code       | character varying(10) | not null
 article    | text                  |
 name       | text                  | not null
 department | character varying(4)  | not null
Indexes:
    "towns_pkey" PRIMARY KEY, btree (id)
    "towns_code_department_key" UNIQUE CONSTRAINT, btree (code, department)
    "towns_id_key" UNIQUE CONSTRAINT, btree (id)

