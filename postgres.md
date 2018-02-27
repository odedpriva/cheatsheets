# postgres

1. dumo db
* pg_dump -h postgres.productionv2.eu-west-1.luminateops.com -U luminate -d ds > outfile

2. list all schema
select schema_name from information_schema.schemata;

3. set schema
SET search_path ="tenant_40bd280367fa11e780dc4e1740089c15_adama";