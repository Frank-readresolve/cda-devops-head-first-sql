# Head first SQL
Discovering SQL through practice.

## Prerequisites
- You should already have a DBeaver project with a configured connection to the "ban" database
- The "ban" database should already have 2 tables `ban_adresses_93` and `ban_adresses_france` in the `public` `schema`
- You should have `26,029,773` rows in the `ban_adresses_france` table

## How to
- Create 2 files in the DBeaver project's `Scripts` folder: `head-first-sql.ddl.sql` and `head-first-sql.dql.sql`
- The `DDL` will contain queries modifying the schema
- The `DQL` will contain queries querying the schema
- In the next section you will find some requirements, each requirement leading to at least one new SQL query to meet the needs
- It's up to you to know in which file goes which query
- Pay attention to aliases in **expected results** section! Your queries should use the same aliases where revelant

## Exercises

### Make a copy
#### Requirements
1. Write a SQL query that creates a new table named `ban_adresses_france_import` from the existing `ban_adresses_france`, copying all its data

#### Expected results
![image](https://github.com/user-attachments/assets/eaca07f1-8270-4ed3-8c72-944172eeb247)

### Verify copy
#### Requirements
1. Write a query that verifies that the number of rows is exactly the same in the newly created table as in the original table

#### Expected results
![image](https://github.com/user-attachments/assets/a41c419d-f0e0-464c-846f-5d89724e5c16)

> [!CAUTION]
> **From now on**, all the queries are to be executed on the new `ban_adresses_france_import` table.

### Schema information
#### Requirements
1. Write a query that retrieves the number of columns in the table
2. Write a query that lists all the table's column names (ascending)

#### Expected results
##### First
![image](https://github.com/user-attachments/assets/56ff10dd-145e-461b-aa57-2261c4c67323)

##### Second
![image](https://github.com/user-attachments/assets/c94434a0-6578-4931-a0f2-37cff27d0025)

### Delete some "useless" columns
#### Requirements
1. Write a query that deletes the columns `code_insee_ancienne_commune` and `nom_ancienne_commune` from the table

#### Expected results
Execute previous "Schema information" queries to check new column number and names.

##### First
![image](https://github.com/user-attachments/assets/1b13a2c0-3ff1-4cd9-8695-7868d6e05b62)

##### Second
![image](https://github.com/user-attachments/assets/27bbacab-d7cd-4686-95d7-8b1db81bd251)

### List ids
#### Requirements
1. Write a query that lists all the `id`s where the `numero` is `0` and `nom_voie` is `Inconnue`, ascending `code_insee`

#### Expected results
![image](https://github.com/user-attachments/assets/94a892af-8e7a-4663-b26a-0d309ee42b63)

### List ids (variation)
#### Requirements
1. Exactly same as previous and the query must return the same result when `nom_voie` is written `INCONNUE`

#### Expected results
![image](https://github.com/user-attachments/assets/ec3da3ea-7b56-49d2-9b99-9e8d5384b212)

### Number of addresses in Corsica
#### Requirements
1. Write a query that retrieves the number of addresses in Corsica

#### Expected results
![image](https://github.com/user-attachments/assets/5dc3e21d-2149-4eb2-99d6-208eadf6e999)

### Top 5
#### Requirements
1. Write a query that retrieves the 5 "greatest" `code_postal` where the addresses' `code_postal` is provided, descending `code_postal`

#### Expected results
![image](https://github.com/user-attachments/assets/8fc3d4f6-70b4-4774-b45f-02ca778b3fa1)

### Top 3
#### Requirements
1. Write a query that retrieves the 3 cities (`code_postal`, `libelle_acheminement`) with the highest number of addresses, indicating the number of addresses (descending)

#### Expected results
![image](https://github.com/user-attachments/assets/6217d927-fce8-4875-82d2-f17ee5dfb447)
