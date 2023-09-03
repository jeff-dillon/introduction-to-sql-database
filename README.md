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
