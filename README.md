Problem Sheet: CouchDB
=====

__*Data Representation and Querying*__

The following exercises are related to the use of the software CouchDB [2]. You can download and use CouchDB on your own devices for free.

1. Run the database, and test your ability to perform a **HTTP** request on it. Do this by performing a **GET** request on it for the root resource.
  *```curl http://127.0.0.1:5984/```
  *```curl -X GET http://127.0.0.1:5984/_all_dbs```

2. Create a new database called **emails**.
  *```curl -X PUT http://127.0.0.1:5984/emails```

3. Create a file called email1.json containing **JSON** representing an email. (You can make up your own properties and values.) Use curl to add email1.json as a document to the
**emails** database.
  *```curl -X POST http://127.0.0.1:5984/emails -H "Content-Type: application/json" -d @emails1.json```

4. Add a second, different document to the database. (Again make up your own properties and values.)
  *```curl -X POST http://127.0.0.1:5984/emails -H "Content-Type: application/json" -d @emails2.json```

5. Retrieve all of the document ids from the database. Then do the same again, except this time including all of the document contents. Finally, individually retrieve each of the documents you created above.
  *```curl -X GET http://127.0.0.1:5984/emails/_all_docs```
  *```curl -X GET http://127.0.0.1:5984/emails/_all_docs?include_docs=true```
  *```curl -X GET http://127.0.0.1:5984/emails/dd9bcc9d87455a292e00dd1058000c0f```

6. Update the first document you created in the database, changing some of the properties in the document. Check to make sure your document has been updated, by retrieving it.
  *```curl -X PUT http://127.0.0.1:5984/emails/1-4374411c22aa641535b27d4fcd1e645d -d @email1v2.json```
  *```{"ok":true,"id":"1-4374411c22aa641535b27d4fcd1e645d","rev":"1-8bae0f862990bcd848aff99b56d97db4"}```
  *```curl -X GET http://127.0.0.1:5984/emails/1-4374411c22aa641535b27d4fcd1e645d```

7. Delete the first document you added to the database, and then retrieve all documents to confirm it has been deleted.
  *```curl -X DELETE http://127.0.0.1:5984/emails/dd9bcc9d87455a292e00dd10580033d9?rev=1-4374411c22aa641535b27d4fcd1e645d```

8. Write a simple CouchApp where users can store JSON objects entered into a tetarea in a web page. [1]
	*bullet point

**References** 

[1] Apache CouchDB 2.0 Documentation. Couchapp.

[2] The Apache Software Foundation. Couchdb.

[3] PouchDB. pouchdb-server.

---
The leading Problem Sheet was assigned as a task to assist the practical learning of Data Representation and Querying, Software Development, GMIT.
