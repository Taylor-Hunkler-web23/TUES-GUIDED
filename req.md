# Requirements
Build an API to support managing pets.
The client wants to:
- save information about their pets. For each pet they'd like to record:
  - name.
  - species (dog, cat, iguana, hamster, fish, horse <- is a horse a pet?).
  - breed (optional, if any).
  - food (what does it eats?)
  - weight (as a floating number)
  - weightUnit (optional, lb, kg)
- see a list of all their pets.
- update their pet's information.
- mark a pet as 'owned' (true/false).
Started an Express JS API.
- npm packages installed: express, helmet, knex, sqlite3 and nodemon as dev dependency.


git init
npm init -y
npx gitignore node
npm i express helmet knex sqlite3
npm i nodemon -D


Migrations are a way to record changes to the database schema.

#It's like git, for the database structure

EVERY CHANGE TO A DATABASE SCHEMA (STRUCTURE) MUST BE DONE WITH A NEW MIGRATION


##Migrations

Initialize knex for our project:npx? knex init

Optionally install knex globally on your system: npm i -g knex or yarn global add knex

-Create a migration: npx knex migrate: make name

Use the migration to declare the changes we plan to make to the schema.

-Run a migration: npx knex migrate:up

-Undo last migration: npx knex migrate down

-Update database to latest changes/migration: npx knex migrate latest  <== multiple new migration

Undo multiple migrations that ran together: npx knex migrate:rollback