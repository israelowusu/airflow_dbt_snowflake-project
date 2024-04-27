use role accountadmin;

create warehouse "your_warehouse_name" with warehouse_size='x-small';
create database "your_db_name";
create role "your_role_name";

show grants on warehouse "your_warehouse_name";

grant usage on warehouse "your_warehouse_name" to role "your_role_name";
grant role "your_role_name" to user "your_snowflake_username";
grant all on database "your_db_name" to role "your_role_name";

use role "your_role_name";

create schema "your_db_name"."your_schema_name";