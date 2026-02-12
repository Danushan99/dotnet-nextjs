# Identity Service
Backend for Kithu community actions.

Next Steps for You:

Navigate to apps/kithu.
Run docker-compose up -d to start the database.
Navigate to apps/kithu/IdentityService.Api.
Run dotnet run.
Open the Swagger UI URL shown in the terminal.
See walkthrough.md for detailed verification steps.

{
  "email": "test@gmail.com",
  "password": "test@123"
}

2. View Tables & Data (To see "Users" table)
While looking at the identity_db container, click on the Exec or Terminal tab.
Type this command to connect to the database:
psql -U admin -d identity_db
To list all tables, type:
\dt
To view data in the Users table (quotes are required!):
SELECT * FROM "Users";
To exit, type \q.


Stop the backend (Ctrl+C).
Reset the Docker Database:
docker-compose down -v
docker-compose up -d
(The -v is important—it deletes the old data so the new table can be created).
Start the backend again:
dotnet run