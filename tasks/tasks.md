# Tasks

## Task 1

### Description

- Setup SGW using setup 1
- Use Postman to check if SGW is working (use Admin PORT)

### Observations

- edit the config.json file and add the line:
  "api": {
      "admin_interface": "0.0.0.0:4985"
    },  


## Task 2

### Description

- Setup SGW using setup 2
- Create a Database using Postman
- Create a Document using Postman
- Get the document using Postman

### Observations

-Both create worked, had to create a bucket
-for get, just had to replace id 2 with 1

## Task 3

### Description

- This task continues from the previous task
- Create a dummy document from CB UI
- Get the document contents using Postman
- Delete the document using Postman

### Observations
- Had to update the bucket config through update API(Change enable shared bucket access)

## Task 4

### Description

- Create a document from Couchbase Server UI
- Review the revision IDs and explain the different values in revision IDs

### Observations
- Revision Id tells us how many times it has been changed

## Task 5

### Description

- Test the following configurations of SGW database:

```
1. enable_shared_bucket_access: false, import_docs: false
2. enable_shared_bucket_access: false, import_docs: true
3. enable_shared_bucket_access: true, import_docs: false
4. enable_shared_bucket_access: true, import_docs: true
```

### Observations

- All worked except the 2nd one, it gives
  "error": "Bad Request",
    "reason": "1 errors:\nInvalid configuration - import_docs enabled, but enable_shared_bucket_access not enabled"
