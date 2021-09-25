# Postgres caruser erstellen:

create user caruser with password '123';
grant all privileges on database cars to caruser;

# Rechte verteilen:

psql -U postgres
\c cars
grant connect on database cars to caruser;
grant all on all tables in schema public to caruser;
