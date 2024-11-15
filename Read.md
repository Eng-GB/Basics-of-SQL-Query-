# Basics of Query
use GB;
show tables from GB;
show columns from responsible;
show columns from students;
show indexes from levels;
alter table levels add index index_lev_name(level_name);

# Queries Commands

select * from levels;

select lev_no, level_name from levels;

select * from address;

# SQL aliases are used to give a table, or a column in a table, a temporary name.

select add_id as ID, district Dagmo, village Xafad from address;

select res_id as ID, res_name Name, res_tell Phone from responsible;

select id as ID, name Name, tell Phone, birth Birth from students;

# Queries by Asc or Desc

select add_id as ID, district Dagmo, village Xaafad, area Zone from address order by add_id asc;

select res_id as ID, res_name Name, res_tell Phone from responsible order by res_name desc;

select res_id as ID, res_name Name, res_tell Phone from responsible order by res_name asc;

# Using Query limit by 123....

select add_id as ID, district Dagmo, village Xafad from address order by add_id desc limit 2;

select * from students limit 5;

select * from address limit 10;

# where select col1,...colum-n from tablename where col relational_operator value

select * from students where birth > 1999;

select * from students where birth = 2000;

select * from address where district = 'kaaraan';

select * from responsible where res_tell <= 600;

select * from responsible where res_id != 2;

select * from students where id = 1 and id > 2;
select * from students where id = 1 or id > 2;

# Using Between

select * from students where birth between '1998-03-10' and '2000-02-10';
select * from students where id between 1 and 2;

# Using Like or not Like

select * from students where name like 'M%';
select * from students where name not like 'C%';

# Using In or not In

select * from address where add_id in (2, 4, 5);
select * from address where district in ('yaqshiid', 'Hilwaa', 'Hilwaa');
select * from address where add_id not in (2, 1);
select * from address where district not in ('yaqshiid', 'Hilwaa');

# Using In  

select * from students where birth is not null;
select * from students where birth is null;
