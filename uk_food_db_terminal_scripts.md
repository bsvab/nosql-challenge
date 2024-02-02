<!-- This file is documenting the terminal code inputs and outputs during the uk_food mongoDB database creation process -->

<!-- establish connection to MongoDB shell -->
(base) brittanysmacbookair: ~ > mongosh
Current Mongosh Log ID:	65bc57d1349a6745b4a515da
Connecting to:		mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.1.1
(node:34494) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
Using MongoDB:		6.0.10
Using Mongosh:		2.1.1

For mongosh info see: https://docs.mongodb.com/mongodb-shell/

------
   The server generated these startup warnings when booting
   2024-01-22T19:25:22.225-06:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
------

<!-- create new database called uk_food -->
test> use uk_food
switched to db uk_food

<!-- create a new collection called establishments -->
uk_food> db.createCollection("establishments")
{ ok: 1 }

<!-- exit the MongoDB shell -->
uk_food> exit

<!-- cd into the 'resources' folder in which the establishments.json is housed -->
(base) brittanysmacbookair: ~ > cd GitHub_Repository_Clones/nosql-challenge/resources/

<!-- import establishments.json into the establishments collection (dropped collection first as a precaution against data duplication) -->
(base) brittanysmacbookair: resources > mongoimport --db uk_food --collection establishments --drop --jsonArray --file establishments.json
2024-02-01T21:27:01.519-0600	connected to: mongodb://localhost/
2024-02-01T21:27:01.520-0600	dropping: uk_food.establishments
2024-02-01T21:27:04.519-0600	[#########...............] uk_food.establishments	15.9MB/39.3MB (40.3%)
2024-02-01T21:27:07.519-0600	[####################....] uk_food.establishments	33.6MB/39.3MB (85.5%)
2024-02-01T21:27:08.697-0600	[########################] uk_food.establishments	39.3MB/39.3MB (100.0%)
2024-02-01T21:27:08.698-0600	39779 document(s) imported successfully. 0 document(s) failed to import.

