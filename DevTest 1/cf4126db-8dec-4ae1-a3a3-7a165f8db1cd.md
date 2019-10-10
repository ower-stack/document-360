Zed’s persistence layer is the owner of the schema, entities and queries. This layer knows the database structure and holds the connection to it.

## Integrated Technologies

Propel	Fast and simple ORM Framework MySQL or PostgreSQL.	Both databases are supported

## Persistence Layer Elements:

| Query container   | A query container holds all the queries in the current module. |
| ----------------- | ------------------------------------------------------------ |
| Entities          | An entity represents a single row from the database.         |
| Queries           | Query objects provide an object-oriented API for writing database queries. |
| Schema definition | Xml-files that define the database schema for the related module. |
| Abstract factory  | The factory is used to instantiate query objects.            |

The following diagram shows how the elements interact:

**See also:**

Database overview
Defining Database Schema
Learn about Entities and their usage
Saving Entities with transactions
Learn about Entity Manager and how to use it
Learn about Repository class and how to use it
Implementing and using a query container
Creating query objects