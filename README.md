Problem Sheet: CouchDB
=====

__*Data Representation and Querying*__

The following exercises are related to the use of the software CouchDB [2]. You can download and use CouchDB on your own devices for free.

1. Run the database, and test your ability to perform a **HTTP** request on it. Do this by performing a **GET** request on it for the root resource.```curl http://127.0.0.1:5984/```

2. Create a new database called **emails**.```curl -X PUT http://127.0.0.1:5984/emails```

3. Create a file called email1.json containing **JSON** representing an email. (You can make up your own properties and values.) Use curl to add email1.json as a document to the
**emails** database.

4. Add a second, different document to the database. (Again make up your own properties
and values.)

5. Retrieve all of the document ids from the database. Then do the same again, except this time including all of the document contents. Finally, individually retrieve each of the documents you created above.

6. Update the first document you created in the database, changing some of the properties in the document. Check to make sure your document has been updated, by retrieving it.

7. Delete the first document you added to the database, and then retrieve all documents to confirm it has been deleted.

8. Write a simple CouchApp where users can store JSON objects entered into a tetarea in a web page. [1]

**References** 

[1] Apache CouchDB 2.0 Documentation. Couchapp.

[2] The Apache Software Foundation. Couchdb.

[3] PouchDB. pouchdb-server.

---
The leading Problem Sheet was assigned as a task to assist the practical learning of Data Representation and Querying, Software Development, GMIT.
