CREATE TABLE mailNotifikation (_guid VARCHAR PRIMARY KEY UNIQUE NOT NULL, _date date, name VARCHAR, fullname VARCHAR, email VARCHAR, password VARCHAR,registered BOOLEAN);

grant insert on mailnotifikation to ckan_default;
grant update on mailnotifikation to ckan_default;
grant select on mailnotifikation to ckan_default;

Add this to CKAN configuration file.
ckan.plugins = ... imailNotifikation
dk.aarhuskommune.odaa_url = postgresql://ckan_default:pass@localhost/odaa_default

Replace pass with the password, you created than you create the user ckan_default.