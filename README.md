# Introduction to SQL: Demo Database
SQLite database for use with the Pluralsight Introduction to SQL course.

## Overview

The Pluuralsight course: "Introduction to SQL" uses a database in the demos
that is not readily available on Pluralsight. This repo contains a SQLite
version of the demo "contacts" database that can be used to follow along with
the demos. 

## Instructions

The easiest way to work with this database is using the SQLTools extension in
VSCode. 

1. Install the SLTools extension.
1. Install the SQLTools SQLite driver
1. Connect to the `contacts.db` database
1. Type your query in the contacts database.session.sql file
1. Execute the query by clicking "run on active connection" 

If you need to refresh the database you can run the `create_db.py` script. This 
will delete and then re-create the database file. 


### Extension Details

| Name | Id | Description | Version | Publisher | Link |
| ---- | -- | ----------- | ------- | --------- | ---- |
| SQLTools | mtxr.sqltools | Connecting users to many of the most commonly used databases. Welcome to database management done right. | 0.27.1 | Matheus Teixeira | [VS Marketplace Link](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools) |
| SQLTools SQLite | mtxr.sqltools-driver-sqlite | SQLTools SQLite | 0.5.0 | Matheus Teixeira | [VS Marketplace Link](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools-driver-sqlite) |

## Schema

The contacts database has the following tables:

### Table: address

| Column | Type | Constraints |
| ------ | ---- | ----------- |
| address_id | INTEGER | PRIMARY KEY |
| address_building_number | VARCHAR(55) | NOT NULL |
| address_street | VARCHAR(55) | NOT NULL |
| address_locality | VARCHAR(55) | |
| address_city | VARCHAR(55) | NOT NULL |
| address_zip_postal | VARCHAR(55) | NOT NULL |
| address_state_province_county | VARCHAR(55) | NOT NULL |
| address_country | VARCHAR(55) | NOT NULL |

### Table: email_address
| Column | Type | Constraints |
| ------ | ---- | ----------- |
| email_address_id | INTEGER | PRIMARY KEY |
| email_address_person_id | INTEGER | FOREIGN KEY |
| email_address | VARCHAR(55) | NOT NULL |

### Table: person
| Column | Type | Constraints |
| ------ | ---- | ----------- |
| person_id | INTEGER | PRIMARY KEY | 
| person_first_name | VARCHAR(55) | NOT NULL |	
| person_last_name | VARCHAR(55) | NOT NULL |	
| person_contacted_number | INTEGER | NOT NULL |
| person_date_last_contacted | DATETIME | NOT NULL |
| person_date_added | DATETIME | NOT NULL |

### Table: person_address
| Column | Type | Constraints |
| ------ | ---- | ----------- |
| person_address_id | INTEGER | PRIMARY KEY |	
| person_address_person_id | INTEGER | FOREIGN KEY |
| person_address_address_id | INTEGER | FOREIGN KEY |

### Table: phone_number
| Column | Type | Constraints |
| ------ | ---- | ----------- |
| phone_number_id | INTEGER | PRIMARY KEY |
| phone_number_person_id | INTEGER | FOREIGN KEY |
| phone_number | VARCHAR(55) | NOT NULL |