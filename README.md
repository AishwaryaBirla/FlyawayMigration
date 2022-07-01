# FlyawayMigration

- Create a Gradle project
- Add flyway dependency
- Write migrations for the following: 

           Create tables
           users(id, name, address)
           products(id, name, price) 

           Alter tables
           Alter ‘name’ field to ‘full_name’ in users table
           Adding primary phone number to the users table

          Create tables
          carts(id, user_id)
          cart_items(id, cart_id, product_id, quantity)
 
 Steps to Complete the Task:
 1. Start by downloading Mysql and install it. 
 2. Make sure Mysql server is running. Then create a gradle project. Add all the required plugins and dependencies. 
 3. Configure the flyway in build.gradle using the url of Mysql (protocol://hostname:port/databasename) and mysql username and password. 
 4. Run the command .gradlew flywayBaseline to first initialize the database. It creates the flyway_schema_history schema in the databse, which keeps te execution status of the flyway migrations
 5. The write flyway migrations in src/main/resources/db/migrations using the naming convectin (V1_1__NameOfTheFile.sql)
 6. Execute the command .gradlew flywayMigrate to run te migrations.
 6. Incase any error occurs, use command .gradlew flywayRepair
 
